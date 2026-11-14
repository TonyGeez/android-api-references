# WebHistoryItem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebHistoryItem

Kotlin| [Java](https://developer.android.com/reference/android/webkit/WebHistoryItem "View this page in Java") 

```
abstract class WebHistoryItem : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.webkit.WebHistoryItem](https://developer.android.com/reference/kotlin/android/webkit/WebHistoryItem#) |

A convenience class for accessing fields in an entry in the back/forward list of a WebView. Each WebHistoryItem is a snapshot of the requested history item.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------|---|
| [WebHistoryItem](https://developer.android.com/reference/kotlin/android/webkit/WebHistoryItem#WebHistoryItem())`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | [getFavicon](https://developer.android.com/reference/kotlin/android/webkit/WebHistoryItem#getFavicon())`()` Return the favicon of this history item or`null`if no favicon was found. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getOriginalUrl](https://developer.android.com/reference/kotlin/android/webkit/WebHistoryItem#getOriginalUrl())`()` Return the original url of this history item. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTitle](https://developer.android.com/reference/kotlin/android/webkit/WebHistoryItem#getTitle())`()` Return the document title of this history item. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getUrl](https://developer.android.com/reference/kotlin/android/webkit/WebHistoryItem#getUrl())`()` Return the url of this history item. |

| Protected methods ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [WebHistoryItem](https://developer.android.com/reference/kotlin/android/webkit/WebHistoryItem#) | [clone](https://developer.android.com/reference/kotlin/android/webkit/WebHistoryItem#clone())`()` Clone the history item for use by clients of WebView. |

## Public constructors

### WebHistoryItem

```
WebHistoryItem()
```

## Public methods

### getFavicon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFavicon(): Bitmap?
```

Return the favicon of this history item or`null`if no favicon was found.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | A Bitmap containing the favicon for this history item or`null`. |

### getOriginalUrl

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getOriginalUrl(): String!
```

Return the original url of this history item. This was the requested url, the final url may be different as there might have been redirects while loading the site.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The original url of this history item. |

### getTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTitle(): String!
```

Return the document title of this history item.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The document title of this history item. |

### getUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUrl(): String!
```

Return the url of this history item. The url is the base url of this history item. See getTargetUrl() for the url that is the actual target of this history item.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The base url of this history item. |

## Protected methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun clone(): WebHistoryItem
```

Clone the history item for use by clients of WebView. On Android 4.4 and later there is no need to use this, as the object is already a read-only copy of the internal state.

| Return ||
|-------------------------------------------------------------------------------------------------|---------------------------|
| [WebHistoryItem](https://developer.android.com/reference/kotlin/android/webkit/WebHistoryItem#) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |
