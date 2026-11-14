# WebResourceError

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebResourceError

Kotlin| [Java](WebResourceError.md) 
| --- | --- |

```
abstract class WebResourceError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.WebResourceError](WebResourceError.md) |

Encapsulates information about errors that occurred during loading of web resources. See [WebViewClient.onReceivedError(WebView, WebResourceRequest, WebResourceError)](WebViewClient.md))

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getDescription](WebResourceError.md))`()` Gets the string describing the error. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](WebResourceError.md))`()` Gets the error code of the error. |

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

Gets the error code of the error. The code corresponds to one of the ERROR_\* constants in [WebViewClient](WebViewClient.md).

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The error code of the error |
