# Browser

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Browser

Kotlin| [Java](https://developer.android.com/reference/android/provider/Browser "View this page in Java") 
| --- | --- |

```
open class Browser
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.Browser](https://developer.android.com/reference/kotlin/android/provider/Browser#) |

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_APPLICATION_ID](https://developer.android.com/reference/kotlin/android/provider/Browser#EXTRA_APPLICATION_ID:kotlin.String) The name of the extra data when starting the Browser from another application. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CREATE_NEW_TAB](https://developer.android.com/reference/kotlin/android/provider/Browser#EXTRA_CREATE_NEW_TAB:kotlin.String) Boolean extra passed along with an Intent to a browser, specifying that a new tab be created. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_HEADERS](https://developer.android.com/reference/kotlin/android/provider/Browser#EXTRA_HEADERS:kotlin.String) The name of the extra data in the VIEW intent. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INITIAL_ZOOM_LEVEL](https://developer.android.com/reference/kotlin/android/provider/Browser#INITIAL_ZOOM_LEVEL:kotlin.String) The name of extra data when starting Browser with ACTION_VIEW or ACTION_SEARCH intent. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------|---|
| [Browser](https://developer.android.com/reference/kotlin/android/provider/Browser#Browser())`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendString](https://developer.android.com/reference/kotlin/android/provider/Browser#sendString(android.content.Context,%20kotlin.String))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `string:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sends the given string using an Intent with [Intent.ACTION_SEND](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEND:kotlin.String) and a mime type of text/plain. |

## Constants

### EXTRA_APPLICATION_ID

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_APPLICATION_ID: String
```

The name of the extra data when starting the Browser from another application.

The value is a unique identification string that will be used to identify the calling application. The Browser will attempt to reuse the same window each time the application launches the Browser with the same identifier. 

 Value: "com.android.browser.application_id"

### EXTRA_CREATE_NEW_TAB

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_CREATE_NEW_TAB: String
```

Boolean extra passed along with an Intent to a browser, specifying that a new tab be created. Overrides EXTRA_APPLICATION_ID; if both are set, a new tab will be used, rather than using the same one. 

 Value: "create_new_tab"

### EXTRA_HEADERS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_HEADERS: String
```

The name of the extra data in the VIEW intent. The data are key/value pairs in the format of Bundle. They will be sent in the HTTP request headers for the provided url. The keys can't be the standard HTTP headers as they are set by the WebView. The url's schema must be http(s).

<br />

 Value: "com.android.browser.headers"

### INITIAL_ZOOM_LEVEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INITIAL_ZOOM_LEVEL: String
```

The name of extra data when starting Browser with ACTION_VIEW or ACTION_SEARCH intent.

The value should be an integer between 0 and 1000. If not set or set to 0, the Browser will use default. If set to 100, the Browser will start with 100%. 

 Value: "browser.initialZoomLevel"

## Public constructors

### Browser

```
Browser()
```

## Public methods

### sendString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun sendString(
    context: Context!, 
    string: String!
): Unit
```

Sends the given string using an Intent with [Intent.ACTION_SEND](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SEND:kotlin.String) and a mime type of text/plain. The string is put into [Intent.EXTRA_TEXT](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_TEXT:kotlin.String).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:the context used to start the activity |
| `string` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to send |
