# JsResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JsResult

Kotlin| [Java](../android/webkit/JsResult.md) 
| --- | --- |

```
open class JsResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.JsResult](../android/webkit/JsResult.md) |

| Known Direct Subclasses [JsPromptResult](../android/webkit/JsPromptResult.md) |------------------------------------------------------------------------------------------------|-------------------------------------------------------| | [JsPromptResult](../android/webkit/JsPromptResult.md) | Public class for handling JavaScript prompt requests. | |
| --- | --- | --- | --- | --- | --- | --- |

An instance of this class is passed as a parameter in various [WebChromeClient](../android/webkit/WebChromeClient.md) action notifications. The object is used as a handle onto the underlying JavaScript-originated request, and provides a means for the client to indicate whether this action should proceed.

## Summary

| Public methods ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](../android/webkit/JsResult.md))`()` Handle the result if the user cancelled the dialog. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [confirm](../android/webkit/JsResult.md))`()` Handle a confirmation response from the user. |

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
