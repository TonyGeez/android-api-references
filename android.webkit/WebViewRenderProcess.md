# WebViewRenderProcess

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebViewRenderProcess

Kotlin| [Java](../android/webkit/WebViewRenderProcess.md) 
| --- | --- |

```
abstract class WebViewRenderProcess
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.WebViewRenderProcess](../android/webkit/WebViewRenderProcess.md) |

WebViewRenderProcess provides an opaque handle to a [WebView](../android/webkit/WebView.md) renderer.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WebViewRenderProcess](../android/webkit/WebViewRenderProcess.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [terminate](../android/webkit/WebViewRenderProcess.md))`()` Cause this renderer to terminate. |

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

Terminating a renderer process may have an effect on multiple [WebView](../android/webkit/WebView.md) instances.

Renderer termination must be handled by properly overriding [WebViewClient.onRenderProcessGone](../android/webkit/WebViewClient.md))for every WebView that shares this renderer. If termination is not handled by all associated WebViews, then the application process will also be terminated.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if it was possible to terminate this renderer,`false`otherwise. |
