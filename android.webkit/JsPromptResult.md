# JsPromptResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JsPromptResult

Kotlin| [Java](JsPromptResult.md) 
| --- | --- |

```
open class JsPromptResult : JsResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.webkit.JsResult](JsResult.md) ||
| | ↳ | [android.webkit.JsPromptResult](JsPromptResult.md) |

Public class for handling JavaScript prompt requests. The WebChromeClient will receive a [WebChromeClient.onJsPrompt(WebView, String, String, String, JsPromptResult)](WebChromeClient.md))call with a JsPromptResult instance as a parameter. This parameter is used to return the result of this user dialog prompt back to the WebView instance. The client can call cancel() to cancel the dialog or confirm() with the user's input to confirm the dialog.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [confirm](JsPromptResult.md))`(`result:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Handle a confirmation response from the user. |

| Inherited functions ||
|---|---|
| From class [JsResult](JsResult.md) |------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](JsResult.md))`()` <br /> Handle the result if the user cancelled the dialog. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [confirm](JsResult.md))`()` <br /> Handle a confirmation response from the user. <br /> | ||

## Public methods

### confirm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun confirm(result: String!): Unit
```

Handle a confirmation response from the user.
