# ServiceWorkerClient

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceWorkerClient

Kotlin| [Java](https://developer.android.com/reference/android/webkit/ServiceWorkerClient "View this page in Java") 

```
open class ServiceWorkerClient
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.webkit.ServiceWorkerClient](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerClient#) |

Base class for clients to capture Service Worker related callbacks, see [ServiceWorkerController](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerController) for usage example.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ServiceWorkerClient](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerClient#ServiceWorkerClient())`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [WebResourceResponse](https://developer.android.com/reference/kotlin/android/webkit/WebResourceResponse)? | [shouldInterceptRequest](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerClient#shouldInterceptRequest(android.webkit.WebResourceRequest))`(`request:` ` [WebResourceRequest](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest)!`)` Notify the host application of a resource request and allow the application to return the data. |

## Public constructors

### ServiceWorkerClient

```
ServiceWorkerClient()
```

## Public methods

### shouldInterceptRequest

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shouldInterceptRequest(request: WebResourceRequest!): WebResourceResponse?
```

Notify the host application of a resource request and allow the application to return the data. If the return value is`null`, the Service Worker will continue to load the resource as usual. Otherwise, the return response and data will be used.

**Note:**This method is called on a thread other than the UI thread so clients should exercise caution when accessing private data or the view system.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `request` | [WebResourceRequest](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest)!:Object containing the details of the request. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WebResourceResponse](https://developer.android.com/reference/kotlin/android/webkit/WebResourceResponse)? | A [android.webkit.WebResourceResponse](https://developer.android.com/reference/kotlin/android/webkit/WebResourceResponse) containing the response information or`null`if the WebView should load the resource itself. |

**See Also**

- [android.webkit.WebViewClient#shouldInterceptRequest(WebView, WebResourceRequest)](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#shouldInterceptRequest(android.webkit.WebView,%20android.webkit.WebResourceRequest))
