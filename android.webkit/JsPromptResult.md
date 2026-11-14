# JsPromptResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JsPromptResult

Kotlin| [Java](https://developer.android.com/reference/android/webkit/JsPromptResult "View this page in Java") 

```
open class JsPromptResult : JsResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.webkit.JsResult](https://developer.android.com/reference/kotlin/android/webkit/JsResult) ||
| | ↳ | [android.webkit.JsPromptResult](https://developer.android.com/reference/kotlin/android/webkit/JsPromptResult#) |

Public class for handling JavaScript prompt requests. The WebChromeClient will receive a [WebChromeClient.onJsPrompt(WebView, String, String, String, JsPromptResult)](https://developer.android.com/reference/kotlin/android/webkit/WebChromeClient#onJsPrompt(android.webkit.WebView,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20android.webkit.JsPromptResult))call with a JsPromptResult instance as a parameter. This parameter is used to return the result of this user dialog prompt back to the WebView instance. The client can call cancel() to cancel the dialog or confirm() with the user's input to confirm the dialog.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [confirm](https://developer.android.com/reference/kotlin/android/webkit/JsPromptResult#confirm(kotlin.String))`(`result:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Handle a confirmation response from the user. |

| Inherited functions ||
|---|---|
| From class [JsResult](https://developer.android.com/reference/kotlin/android/webkit/JsResult) |------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/webkit/JsResult#cancel())`()` <br /> Handle the result if the user cancelled the dialog. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [confirm](https://developer.android.com/reference/kotlin/android/webkit/JsResult#confirm())`()` <br /> Handle a confirmation response from the user. <br /> | ||

## Public methods

### confirm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun confirm(result: String!): Unit
```

Handle a confirmation response from the user.
