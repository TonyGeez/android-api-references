# WebIconDatabase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebIconDatabase

Kotlin| [Java](../android/webkit/WebIconDatabase.md) 
| --- | --- |

```
abstract class WebIconDatabase
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.WebIconDatabase](../android/webkit/WebIconDatabase.md) |

| **This class was deprecated in API level 18.**
|
| This class is only required when running on devices up to [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md)

Functions for manipulating the icon database used by WebView. These functions require that a WebView be constructed before being invoked and WebView.getIconDatabase() will return a WebIconDatabase object. This WebIconDatabase object is a single instance and all methods operate on that single object. The main use-case for this class is calling [open](../android/webkit/WebIconDatabase.md))to enable favicon functionality on all WebView instances in this process.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [IconListener](../android/webkit/WebIconDatabase.IconListener.md) Interface for receiving icons from the database. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------|---|
| [WebIconDatabase](../android/webkit/WebIconDatabase.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/webkit/WebIconDatabase.md))`()` Close the shared instance of the icon database. |
| openstatic [WebIconDatabase](../android/webkit/WebIconDatabase.md)! | [getInstance](../android/webkit/WebIconDatabase.md))`()` Get the global instance of WebIconDatabase. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [open](../android/webkit/WebIconDatabase.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Open a the icon database and store the icons in the given path. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseIconForPageUrl](../android/webkit/WebIconDatabase.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Release the icon for the given page url. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAllIcons](../android/webkit/WebIconDatabase.md))`()` Removes all the icons in the database. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestIconForPageUrl](../android/webkit/WebIconDatabase.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `listener:` ` [WebIconDatabase.IconListener](../android/webkit/WebIconDatabase.IconListener.md)!`)` Request the Bitmap representing the icon for the given page url. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [retainIconForPageUrl](../android/webkit/WebIconDatabase.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retain the icon for the given page url. |

## Public constructors

### WebIconDatabase

```
WebIconDatabase()
```

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

**Deprecated:** *Deprecated in Java.*

Close the shared instance of the icon database. 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(): WebIconDatabase!
```

**Deprecated:** *Deprecated in Java.*

Get the global instance of WebIconDatabase.

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [WebIconDatabase](../android/webkit/WebIconDatabase.md)! | A single instance of WebIconDatabase. It will be the same instance for the current process each time this method is called. |

### open

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun open(path: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Open a the icon database and store the icons in the given path.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The directory path where the icon database will be stored. |

### releaseIconForPageUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun releaseIconForPageUrl(url: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Release the icon for the given page url.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The page's url. |

### removeAllIcons

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeAllIcons(): Unit
```

**Deprecated:** *Deprecated in Java.*

Removes all the icons in the database. 

### requestIconForPageUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun requestIconForPageUrl(
    url: String!, 
    listener: WebIconDatabase.IconListener!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Request the Bitmap representing the icon for the given page url. If the icon exists, the listener will be called with the result.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The page's url. |
| `listener` | [WebIconDatabase.IconListener](../android/webkit/WebIconDatabase.IconListener.md)!:An implementation on IconListener to receive the result. |

### retainIconForPageUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun retainIconForPageUrl(url: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Retain the icon for the given page url.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The page's url. |
