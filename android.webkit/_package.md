# android.webkit

# android.webkit

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [DownloadListener](DownloadListener.md) | <br /> |
| --- | --- |
| [Callback](../android/webkit/GeolocationPermissions.Callback.md) | A callback interface used by the host application to set the Geolocation permission state for an origin. |
| [PluginStub](PluginStub.md) | This interface is used to implement plugins in a WebView. |
| [ValueCallback](ValueCallback.md) | A callback interface used to provide values asynchronously. |
| --- | --- |
| [CustomViewCallback](../android/webkit/WebChromeClient.CustomViewCallback.md) | A callback interface used by the host application to notify the current page that its custom view has been dismissed. |
| [IconListener](../android/webkit/WebIconDatabase.IconListener.md) | Interface for receiving icons from the database. |
| [WebResourceRequest](WebResourceRequest.md) | Encompasses parameters to the android. |
| --- | --- |
| [QuotaUpdater](../android/webkit/WebStorage.QuotaUpdater.md) | Encapsulates a callback function which is used to provide a new quota for a JavaScript storage API. |
| [FindListener](../android/webkit/WebView.FindListener.md) | Interface to listen for find results. |
| [PictureListener](../android/webkit/WebView.PictureListener.md) | Interface to listen for new pictures as they change. |
| --- | --- |

## Classes

| [ClientCertRequest](ClientCertRequest.md) | ClientCertRequest: The user receives an instance of this class as a parameter of [WebViewClient.onReceivedClientCertRequest](WebViewClient.md)). |
| --- | --- |
| [ConsoleMessage](ConsoleMessage.md) | Public class representing a JavaScript console message from WebCore. |
| [CookieManager](CookieManager.md) | Manages the cookies used by an application's [WebView](WebView.md) instances. |
| [CookieSyncManager](CookieSyncManager.md) | The CookieSyncManager is used to synchronize the browser cookie store between RAM and permanent storage. |
| --- | --- |
| [DateSorter](DateSorter.md) | Sorts dates into the following groups: Today Yesterday seven days ago one month ago older than a month ago |
| [GeolocationPermissions](GeolocationPermissions.md) | This class is used to manage permissions for the WebView's Geolocation JavaScript API. |
| [HttpAuthHandler](HttpAuthHandler.md) | Represents a request for HTTP authentication. |
| --- | --- |
| [JsPromptResult](JsPromptResult.md) | Public class for handling JavaScript prompt requests. |
| [JsResult](JsResult.md) | An instance of this class is passed as a parameter in various [WebChromeClient](WebChromeClient.md) action notifications. |
| [MimeTypeMap](MimeTypeMap.md) | Two-way map that maps MIME-types to file extensions and vice versa. |
| --- | --- |
| [PermissionRequest](PermissionRequest.md) | This class defines a permission request and is used when web content requests access to protected resources. |
| [RenderProcessGoneDetail](RenderProcessGoneDetail.md) | This class provides more specific information about why the render process exited. |
| [SafeBrowsingResponse](SafeBrowsingResponse.md) | Used to indicate an action to take when hitting a malicious URL. |
| --- | --- |
| [ServiceWorkerClient](ServiceWorkerClient.md) | Base class for clients to capture Service Worker related callbacks, see [ServiceWorkerController](ServiceWorkerController.md) for usage example. |
| [ServiceWorkerController](ServiceWorkerController.md) | Manages Service Workers used by WebView. |
| [ServiceWorkerWebSettings](ServiceWorkerWebSettings.md) | Manages settings state for all Service Workers. |
| --- | --- |
| [SslErrorHandler](SslErrorHandler.md) | Represents a request for handling an SSL error. |
| [TracingConfig](TracingConfig.md) | Holds tracing configuration information and predefined settings. |
| [TracingController](TracingController.md) | Manages tracing of WebViews. |
| --- | --- |
| [URLUtil](URLUtil.md) | <br /> |
| [WebBackForwardList](WebBackForwardList.md) | This class contains the back/forward list for a WebView. |
| [WebChromeClient](WebChromeClient.md) | <br /> |
| --- | --- |
| [WebHistoryItem](WebHistoryItem.md) | A convenience class for accessing fields in an entry in the back/forward list of a WebView. |
| [WebIconDatabase](WebIconDatabase.md) | Functions for manipulating the icon database used by WebView. |
| [WebMessage](WebMessage.md) | The Java representation of the HTML5 PostMessage event. |
| --- | --- |
| [WebMessagePort](WebMessagePort.md) | The Java representation of the [HTML5 message ports.](https://html.spec.whatwg.org/multipage/comms.html#messageport) |
| [WebResourceError](WebResourceError.md) | Encapsulates information about errors that occurred during loading of web resources. |
| [WebResourceResponse](WebResourceResponse.md) | Encapsulates a resource response. |
| --- | --- |
| [WebSettings](WebSettings.md) | Manages settings state for a WebView. |
| [WebStorage](WebStorage.md) | This class is used to manage the JavaScript storage APIs provided by the [WebView](WebView.md). |
| [WebView](WebView.md) | A View that displays web pages. |
| --- | --- |
| [WebViewClient](WebViewClient.md) | <br /> |
| [WebViewDatabase](WebViewDatabase.md) | This class allows developers to determine whether any WebView used in the application has stored any of the following types of browsing data and to clear any such stored data for all WebViews in the application. |
| [WebViewFragment](WebViewFragment.md) | A fragment that displays a WebView. |
| --- | --- |
| [WebViewRenderProcess](WebViewRenderProcess.md) | WebViewRenderProcess provides an opaque handle to a [WebView](WebView.md) renderer. |
| [WebViewRenderProcessClient](WebViewRenderProcessClient.md) | Used to receive callbacks on [WebView](WebView.md) renderer events. |

## Annotations

| [JavascriptInterface](JavascriptInterface.md) | Annotation that allows exposing methods to JavaScript. |
| --- | --- |
