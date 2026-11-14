# WebResourceError

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebResourceError

Kotlin| [Java](https://developer.android.com/reference/android/webkit/WebResourceError "View this page in Java") 
| --- | --- |

```
abstract class WebResourceError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.WebResourceError](https://developer.android.com/reference/kotlin/android/webkit/WebResourceError#) |

Encapsulates information about errors that occurred during loading of web resources. See [WebViewClient.onReceivedError(WebView, WebResourceRequest, WebResourceError)](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onReceivedError(android.webkit.WebView,%20android.webkit.WebResourceRequest,%20android.webkit.WebResourceError))

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getDescription](https://developer.android.com/reference/kotlin/android/webkit/WebResourceError#getDescription())`()` Gets the string describing the error. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](https://developer.android.com/reference/kotlin/android/webkit/WebResourceError#getErrorCode())`()` Gets the error code of the error. |

## Public methods

### getDescription

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDescription(): CharSequence!
```

Gets the string describing the error. Descriptions are localized, and thus can be used for communicating the problem to the user.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | The description of the error |

### getErrorCode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getErrorCode(): Int
```

Gets the error code of the error. The code corresponds to one of the ERROR_\* constants in [WebViewClient](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient).

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The error code of the error |
