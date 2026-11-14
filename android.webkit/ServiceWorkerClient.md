# ServiceWorkerClient

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceWorkerClient

Kotlin| [Java](ServiceWorkerClient.md) 
| --- | --- |

```
open class ServiceWorkerClient
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.ServiceWorkerClient](ServiceWorkerClient.md) |

Base class for clients to capture Service Worker related callbacks, see [ServiceWorkerController](ServiceWorkerController.md) for usage example.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ServiceWorkerClient](ServiceWorkerClient.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [WebResourceResponse](WebResourceResponse.md)? | [shouldInterceptRequest](ServiceWorkerClient.md))`(`request:` ` [WebResourceRequest](WebResourceRequest.md)!`)` Notify the host application of a resource request and allow the application to return the data. |

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
| `request` | [WebResourceRequest](WebResourceRequest.md)!:Object containing the details of the request. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WebResourceResponse](WebResourceResponse.md)? | A [android.webkit.WebResourceResponse](WebResourceResponse.md) containing the response information or`null`if the WebView should load the resource itself. |

**See Also**

- [android.webkit.WebViewClient#shouldInterceptRequest(WebView, WebResourceRequest)](WebViewClient.md))
