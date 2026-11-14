# android.webkit

# android.webkit

Kotlin| [Java](../android/webkit/_package.md)
| --- | --- |

## Interfaces

| [DownloadListener](../android/webkit/DownloadListener.md) | <br /> |
| --- | --- |
| [Callback](../android/webkit/GeolocationPermissions.Callback.md) | A callback interface used by the host application to set the Geolocation permission state for an origin. |
| [PluginStub](../android/webkit/PluginStub.md) | This interface is used to implement plugins in a WebView. |
| [ValueCallback](../android/webkit/ValueCallback.md) | A callback interface used to provide values asynchronously. |
| --- | --- |
| [CustomViewCallback](../android/webkit/WebChromeClient.CustomViewCallback.md) | A callback interface used by the host application to notify the current page that its custom view has been dismissed. |
| [IconListener](../android/webkit/WebIconDatabase.IconListener.md) | Interface for receiving icons from the database. |
| [WebResourceRequest](../android/webkit/WebResourceRequest.md) | Encompasses parameters to the android. |
| --- | --- |
| [QuotaUpdater](../android/webkit/WebStorage.QuotaUpdater.md) | Encapsulates a callback function which is used to provide a new quota for a JavaScript storage API. |
| [FindListener](../android/webkit/WebView.FindListener.md) | Interface to listen for find results. |
| [PictureListener](../android/webkit/WebView.PictureListener.md) | Interface to listen for new pictures as they change. |
| --- | --- |

## Classes

| [ClientCertRequest](../android/webkit/ClientCertRequest.md) | ClientCertRequest: The user receives an instance of this class as a parameter of [WebViewClient.onReceivedClientCertRequest](../android/webkit/WebViewClient.md)). |
| --- | --- |
| [ConsoleMessage](../android/webkit/ConsoleMessage.md) | Public class representing a JavaScript console message from WebCore. |
| [CookieManager](../android/webkit/CookieManager.md) | Manages the cookies used by an application's [WebView](../android/webkit/WebView.md) instances. |
| [CookieSyncManager](../android/webkit/CookieSyncManager.md) | The CookieSyncManager is used to synchronize the browser cookie store between RAM and permanent storage. |
| --- | --- |
| [DateSorter](../android/webkit/DateSorter.md) | Sorts dates into the following groups: Today Yesterday seven days ago one month ago older than a month ago |
| [GeolocationPermissions](../android/webkit/GeolocationPermissions.md) | This class is used to manage permissions for the WebView's Geolocation JavaScript API. |
| [HttpAuthHandler](../android/webkit/HttpAuthHandler.md) | Represents a request for HTTP authentication. |
| --- | --- |
| [JsPromptResult](../android/webkit/JsPromptResult.md) | Public class for handling JavaScript prompt requests. |
| [JsResult](../android/webkit/JsResult.md) | An instance of this class is passed as a parameter in various [WebChromeClient](../android/webkit/WebChromeClient.md) action notifications. |
| [MimeTypeMap](../android/webkit/MimeTypeMap.md) | Two-way map that maps MIME-types to file extensions and vice versa. |
| --- | --- |
| [PermissionRequest](../android/webkit/PermissionRequest.md) | This class defines a permission request and is used when web content requests access to protected resources. |
| [RenderProcessGoneDetail](../android/webkit/RenderProcessGoneDetail.md) | This class provides more specific information about why the render process exited. |
| [SafeBrowsingResponse](../android/webkit/SafeBrowsingResponse.md) | Used to indicate an action to take when hitting a malicious URL. |
| --- | --- |
| [ServiceWorkerClient](../android/webkit/ServiceWorkerClient.md) | Base class for clients to capture Service Worker related callbacks, see [ServiceWorkerController](../android/webkit/ServiceWorkerController.md) for usage example. |
| [ServiceWorkerController](../android/webkit/ServiceWorkerController.md) | Manages Service Workers used by WebView. |
| [ServiceWorkerWebSettings](../android/webkit/ServiceWorkerWebSettings.md) | Manages settings state for all Service Workers. |
| --- | --- |
| [SslErrorHandler](../android/webkit/SslErrorHandler.md) | Represents a request for handling an SSL error. |
| [TracingConfig](../android/webkit/TracingConfig.md) | Holds tracing configuration information and predefined settings. |
| [TracingController](../android/webkit/TracingController.md) | Manages tracing of WebViews. |
| --- | --- |
| [URLUtil](../android/webkit/URLUtil.md) | <br /> |
| [WebBackForwardList](../android/webkit/WebBackForwardList.md) | This class contains the back/forward list for a WebView. |
| [WebChromeClient](../android/webkit/WebChromeClient.md) | <br /> |
| --- | --- |
| [WebHistoryItem](../android/webkit/WebHistoryItem.md) | A convenience class for accessing fields in an entry in the back/forward list of a WebView. |
| [WebIconDatabase](../android/webkit/WebIconDatabase.md) | Functions for manipulating the icon database used by WebView. |
| [WebMessage](../android/webkit/WebMessage.md) | The Java representation of the HTML5 PostMessage event. |
| --- | --- |
| [WebMessagePort](../android/webkit/WebMessagePort.md) | The Java representation of the [HTML5 message ports.](https://html.spec.whatwg.org/multipage/comms.html#messageport) |
| [WebResourceError](../android/webkit/WebResourceError.md) | Encapsulates information about errors that occurred during loading of web resources. |
| [WebResourceResponse](../android/webkit/WebResourceResponse.md) | Encapsulates a resource response. |
| --- | --- |
| [WebSettings](../android/webkit/WebSettings.md) | Manages settings state for a WebView. |
| [WebStorage](../android/webkit/WebStorage.md) | This class is used to manage the JavaScript storage APIs provided by the [WebView](../android/webkit/WebView.md). |
| [WebView](../android/webkit/WebView.md) | A View that displays web pages. |
| --- | --- |
| [WebViewClient](../android/webkit/WebViewClient.md) | <br /> |
| [WebViewDatabase](../android/webkit/WebViewDatabase.md) | This class allows developers to determine whether any WebView used in the application has stored any of the following types of browsing data and to clear any such stored data for all WebViews in the application. |
| [WebViewFragment](../android/webkit/WebViewFragment.md) | A fragment that displays a WebView. |
| --- | --- |
| [WebViewRenderProcess](../android/webkit/WebViewRenderProcess.md) | WebViewRenderProcess provides an opaque handle to a [WebView](../android/webkit/WebView.md) renderer. |
| [WebViewRenderProcessClient](../android/webkit/WebViewRenderProcessClient.md) | Used to receive callbacks on [WebView](../android/webkit/WebView.md) renderer events. |

## Annotations

| [JavascriptInterface](../android/webkit/JavascriptInterface.md) | Annotation that allows exposing methods to JavaScript. |
| --- | --- |
