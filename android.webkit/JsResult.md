# JsResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JsResult

Kotlin| [Java](https://developer.android.com/reference/android/webkit/JsResult "View this page in Java") 
| --- | --- |

```
open class JsResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.JsResult](https://developer.android.com/reference/kotlin/android/webkit/JsResult#) |

| Known Direct Subclasses [JsPromptResult](https://developer.android.com/reference/kotlin/android/webkit/JsPromptResult) |------------------------------------------------------------------------------------------------|-------------------------------------------------------| | [JsPromptResult](https://developer.android.com/reference/kotlin/android/webkit/JsPromptResult) | Public class for handling JavaScript prompt requests. | |
| --- | --- | --- | --- | --- | --- | --- |

An instance of this class is passed as a parameter in various [WebChromeClient](https://developer.android.com/reference/kotlin/android/webkit/WebChromeClient) action notifications. The object is used as a handle onto the underlying JavaScript-originated request, and provides a means for the client to indicate whether this action should proceed.

## Summary

| Public methods ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/webkit/JsResult#cancel())`()` Handle the result if the user cancelled the dialog. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [confirm](https://developer.android.com/reference/kotlin/android/webkit/JsResult#confirm())`()` Handle a confirmation response from the user. |

## Public methods

### cancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun cancel(): Unit
```

Handle the result if the user cancelled the dialog. 

### confirm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun confirm(): Unit
```

Handle a confirmation response from the user.
