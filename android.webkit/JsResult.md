# JsResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JsResult

Kotlin| [Java](JsResult.md) 
| --- | --- |

```
open class JsResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.JsResult](JsResult.md) |

| Known Direct Subclasses [JsPromptResult](JsPromptResult.md) |------------------------------------------------------------------------------------------------|-------------------------------------------------------| | [JsPromptResult](JsPromptResult.md) | Public class for handling JavaScript prompt requests. | |
| --- | --- | --- | --- | --- | --- | --- |

An instance of this class is passed as a parameter in various [WebChromeClient](WebChromeClient.md) action notifications. The object is used as a handle onto the underlying JavaScript-originated request, and provides a means for the client to indicate whether this action should proceed.

## Summary

| Public methods ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](JsResult.md))`()` Handle the result if the user cancelled the dialog. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [confirm](JsResult.md))`()` Handle a confirmation response from the user. |

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
