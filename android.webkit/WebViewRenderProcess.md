# WebViewRenderProcess

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebViewRenderProcess

Kotlin| [Java](WebViewRenderProcess.md) 
| --- | --- |

```
abstract class WebViewRenderProcess
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.WebViewRenderProcess](WebViewRenderProcess.md) |

WebViewRenderProcess provides an opaque handle to a [WebView](WebView.md) renderer.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WebViewRenderProcess](WebViewRenderProcess.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [terminate](WebViewRenderProcess.md))`()` Cause this renderer to terminate. |

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

Terminating a renderer process may have an effect on multiple [WebView](WebView.md) instances.

Renderer termination must be handled by properly overriding [WebViewClient.onRenderProcessGone](WebViewClient.md))for every WebView that shares this renderer. If termination is not handled by all associated WebViews, then the application process will also be terminated.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if it was possible to terminate this renderer,`false`otherwise. |
