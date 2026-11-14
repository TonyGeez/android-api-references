# WebViewRenderProcess

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebViewRenderProcess

Kotlin| [Java](https://developer.android.com/reference/android/webkit/WebViewRenderProcess "View this page in Java") 
| --- | --- |

```
abstract class WebViewRenderProcess
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.WebViewRenderProcess](https://developer.android.com/reference/kotlin/android/webkit/WebViewRenderProcess#) |

WebViewRenderProcess provides an opaque handle to a [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView) renderer.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WebViewRenderProcess](https://developer.android.com/reference/kotlin/android/webkit/WebViewRenderProcess#WebViewRenderProcess())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [terminate](https://developer.android.com/reference/kotlin/android/webkit/WebViewRenderProcess#terminate())`()` Cause this renderer to terminate. |

## Public constructors

### WebViewRenderProcess

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WebViewRenderProcess()
```

## Public methods

### terminate

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun terminate(): Boolean
```

Cause this renderer to terminate.

Calling this on a not yet started, or an already terminated renderer will have no effect.

Terminating a renderer process may have an effect on multiple [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView) instances.

Renderer termination must be handled by properly overriding [WebViewClient.onRenderProcessGone](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onRenderProcessGone(android.webkit.WebView,%20android.webkit.RenderProcessGoneDetail))for every WebView that shares this renderer. If termination is not handled by all associated WebViews, then the application process will also be terminated.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if it was possible to terminate this renderer,`false`otherwise. |
