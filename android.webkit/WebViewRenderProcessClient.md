# WebViewRenderProcessClient

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebViewRenderProcessClient

Kotlin | [Java](../android/webkit/WebViewRenderProcessClient.md) 
| --- | --- |

```
abstract class WebViewRenderProcessClient
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.WebViewRenderProcessClient](../android/webkit/WebViewRenderProcessClient.md) |

Used to receive callbacks on [WebView](../android/webkit/WebView.md) renderer events. WebViewRenderProcessClient instances may be set or retrieved via [android.webkit.WebView#setWebViewRenderProcessClient(android.webkit.WebViewRenderProcessClient)](../android/webkit/WebView.md)) and [android.webkit.WebView#getWebViewRenderProcessClient()](../android/webkit/WebView.md)). Instances may be attached to multiple WebViews, and thus a single renderer event may cause a callback to be called multiple times with different WebView parameters.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WebViewRenderProcessClient](../android/webkit/WebViewRenderProcessClient.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRenderProcessResponsive](../android/webkit/WebViewRenderProcessClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)`, `renderer:` ` [WebViewRenderProcess](../android/webkit/WebViewRenderProcess.md)?`)` Called once when an unresponsive renderer currently associated with `view` becomes responsive. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRenderProcessUnresponsive](../android/webkit/WebViewRenderProcessClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)`, `renderer:` ` [WebViewRenderProcess](../android/webkit/WebViewRenderProcess.md)?`)` Called when the renderer currently associated with `view` becomes unresponsive as a result of a long running blocking task such as the execution of JavaScript. |

## Public constructors

### WebViewRenderProcessClient

```
WebViewRenderProcessClient()
```

## Public methods

### onRenderProcessResponsive

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onRenderProcessResponsive(
    view: WebView, 
    renderer: WebViewRenderProcess?
): Unit
```

Called once when an unresponsive renderer currently associated with `view` becomes responsive.

After a WebView renderer becomes unresponsive, which is notified to the application by [WebViewRenderProcessClient.onRenderProcessUnresponsive](../android/webkit/WebViewRenderProcessClient.md)), it is possible for the blocking renderer task to complete, returning the renderer to a responsive state. In that case, this method is called once to indicate responsiveness.

No action is taken by WebView as a result of this method call.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md): The [WebView](../android/webkit/WebView.md) for which responsiveness was detected. This value cannot be `null`. |
| `renderer` | [WebViewRenderProcess](../android/webkit/WebViewRenderProcess.md)?: The [WebViewRenderProcess](../android/webkit/WebViewRenderProcess.md) that has become responsive, or `null` if WebView is running in single process mode. |

### onRenderProcessUnresponsive

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onRenderProcessUnresponsive(
    view: WebView, 
    renderer: WebViewRenderProcess?
): Unit
```

Called when the renderer currently associated with `view` becomes unresponsive as a result of a long running blocking task such as the execution of JavaScript.

If a WebView fails to process an input event, or successfully navigate to a new URL within a reasonable time frame, the renderer is considered to be unresponsive, and this callback will be called.

This callback will continue to be called at regular intervals as long as the renderer remains unresponsive. If the renderer becomes responsive again, [android.webkit.WebViewRenderProcessClient#onRenderProcessResponsive](../android/webkit/WebViewRenderProcessClient.md)) will be called once, and this method will not subsequently be called unless another period of unresponsiveness is detected.

The minimum interval between successive calls to `onRenderProcessUnresponsive` is 5 seconds.

No action is taken by WebView as a result of this method call. Applications may choose to terminate the associated renderer via the object that is passed to this callback, if in multiprocess mode, however this must be accompanied by correctly handling [WebViewClient.onRenderProcessGone](../android/webkit/WebViewClient.md)) for this WebView, and all other WebViews associated with the same renderer. Failure to do so will result in application termination.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md): The [WebView](../android/webkit/WebView.md) for which unresponsiveness was detected. This value cannot be `null`. |
| `renderer` | [WebViewRenderProcess](../android/webkit/WebViewRenderProcess.md)?: The [WebViewRenderProcess](../android/webkit/WebViewRenderProcess.md) that has become unresponsive, or `null` if WebView is running in single process mode. |
