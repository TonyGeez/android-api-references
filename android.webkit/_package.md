# android.webkit

# android.webkit

Kotlin| [Java](https://developer.android.com/reference/android/webkit/package-summary "View this page in Java")

## Interfaces

| [DownloadListener](https://developer.android.com/reference/kotlin/android/webkit/DownloadListener) | <br /> |
| [Callback](https://developer.android.com/reference/kotlin/android/webkit/GeolocationPermissions.Callback) | A callback interface used by the host application to set the Geolocation permission state for an origin. |
| [PluginStub](https://developer.android.com/reference/kotlin/android/webkit/PluginStub) | This interface is used to implement plugins in a WebView. |
| [ValueCallback](https://developer.android.com/reference/kotlin/android/webkit/ValueCallback) | A callback interface used to provide values asynchronously. |
| [CustomViewCallback](https://developer.android.com/reference/kotlin/android/webkit/WebChromeClient.CustomViewCallback) | A callback interface used by the host application to notify the current page that its custom view has been dismissed. |
| [IconListener](https://developer.android.com/reference/kotlin/android/webkit/WebIconDatabase.IconListener) | Interface for receiving icons from the database. |
| [WebResourceRequest](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest) | Encompasses parameters to the android. |
| [QuotaUpdater](https://developer.android.com/reference/kotlin/android/webkit/WebStorage.QuotaUpdater) | Encapsulates a callback function which is used to provide a new quota for a JavaScript storage API. |
| [FindListener](https://developer.android.com/reference/kotlin/android/webkit/WebView.FindListener) | Interface to listen for find results. |
| [PictureListener](https://developer.android.com/reference/kotlin/android/webkit/WebView.PictureListener) | Interface to listen for new pictures as they change. |

## Classes

| [ClientCertRequest](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest) | ClientCertRequest: The user receives an instance of this class as a parameter of [WebViewClient.onReceivedClientCertRequest](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onReceivedClientCertRequest(android.webkit.WebView,%20android.webkit.ClientCertRequest)). |
| [ConsoleMessage](https://developer.android.com/reference/kotlin/android/webkit/ConsoleMessage) | Public class representing a JavaScript console message from WebCore. |
| [CookieManager](https://developer.android.com/reference/kotlin/android/webkit/CookieManager) | Manages the cookies used by an application's [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView) instances. |
| [CookieSyncManager](https://developer.android.com/reference/kotlin/android/webkit/CookieSyncManager) | The CookieSyncManager is used to synchronize the browser cookie store between RAM and permanent storage. |
| [DateSorter](https://developer.android.com/reference/kotlin/android/webkit/DateSorter) | Sorts dates into the following groups: Today Yesterday seven days ago one month ago older than a month ago |
| [GeolocationPermissions](https://developer.android.com/reference/kotlin/android/webkit/GeolocationPermissions) | This class is used to manage permissions for the WebView's Geolocation JavaScript API. |
| [HttpAuthHandler](https://developer.android.com/reference/kotlin/android/webkit/HttpAuthHandler) | Represents a request for HTTP authentication. |
| [JsPromptResult](https://developer.android.com/reference/kotlin/android/webkit/JsPromptResult) | Public class for handling JavaScript prompt requests. |
| [JsResult](https://developer.android.com/reference/kotlin/android/webkit/JsResult) | An instance of this class is passed as a parameter in various [WebChromeClient](https://developer.android.com/reference/kotlin/android/webkit/WebChromeClient) action notifications. |
| [MimeTypeMap](https://developer.android.com/reference/kotlin/android/webkit/MimeTypeMap) | Two-way map that maps MIME-types to file extensions and vice versa. |
| [PermissionRequest](https://developer.android.com/reference/kotlin/android/webkit/PermissionRequest) | This class defines a permission request and is used when web content requests access to protected resources. |
| [RenderProcessGoneDetail](https://developer.android.com/reference/kotlin/android/webkit/RenderProcessGoneDetail) | This class provides more specific information about why the render process exited. |
| [SafeBrowsingResponse](https://developer.android.com/reference/kotlin/android/webkit/SafeBrowsingResponse) | Used to indicate an action to take when hitting a malicious URL. |
| [ServiceWorkerClient](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerClient) | Base class for clients to capture Service Worker related callbacks, see [ServiceWorkerController](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerController) for usage example. |
| [ServiceWorkerController](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerController) | Manages Service Workers used by WebView. |
| [ServiceWorkerWebSettings](https://developer.android.com/reference/kotlin/android/webkit/ServiceWorkerWebSettings) | Manages settings state for all Service Workers. |
| [SslErrorHandler](https://developer.android.com/reference/kotlin/android/webkit/SslErrorHandler) | Represents a request for handling an SSL error. |
| [TracingConfig](https://developer.android.com/reference/kotlin/android/webkit/TracingConfig) | Holds tracing configuration information and predefined settings. |
| [TracingController](https://developer.android.com/reference/kotlin/android/webkit/TracingController) | Manages tracing of WebViews. |
| [URLUtil](https://developer.android.com/reference/kotlin/android/webkit/URLUtil) | <br /> |
| [WebBackForwardList](https://developer.android.com/reference/kotlin/android/webkit/WebBackForwardList) | This class contains the back/forward list for a WebView. |
| [WebChromeClient](https://developer.android.com/reference/kotlin/android/webkit/WebChromeClient) | <br /> |
| [WebHistoryItem](https://developer.android.com/reference/kotlin/android/webkit/WebHistoryItem) | A convenience class for accessing fields in an entry in the back/forward list of a WebView. |
| [WebIconDatabase](https://developer.android.com/reference/kotlin/android/webkit/WebIconDatabase) | Functions for manipulating the icon database used by WebView. |
| [WebMessage](https://developer.android.com/reference/kotlin/android/webkit/WebMessage) | The Java representation of the HTML5 PostMessage event. |
| [WebMessagePort](https://developer.android.com/reference/kotlin/android/webkit/WebMessagePort) | The Java representation of the [HTML5 message ports.](https://html.spec.whatwg.org/multipage/comms.html#messageport) |
| [WebResourceError](https://developer.android.com/reference/kotlin/android/webkit/WebResourceError) | Encapsulates information about errors that occurred during loading of web resources. |
| [WebResourceResponse](https://developer.android.com/reference/kotlin/android/webkit/WebResourceResponse) | Encapsulates a resource response. |
| [WebSettings](https://developer.android.com/reference/kotlin/android/webkit/WebSettings) | Manages settings state for a WebView. |
| [WebStorage](https://developer.android.com/reference/kotlin/android/webkit/WebStorage) | This class is used to manage the JavaScript storage APIs provided by the [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView). |
| [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView) | A View that displays web pages. |
| [WebViewClient](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient) | <br /> |
| [WebViewDatabase](https://developer.android.com/reference/kotlin/android/webkit/WebViewDatabase) | This class allows developers to determine whether any WebView used in the application has stored any of the following types of browsing data and to clear any such stored data for all WebViews in the application. |
| [WebViewFragment](https://developer.android.com/reference/kotlin/android/webkit/WebViewFragment) | A fragment that displays a WebView. |
| [WebViewRenderProcess](https://developer.android.com/reference/kotlin/android/webkit/WebViewRenderProcess) | WebViewRenderProcess provides an opaque handle to a [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView) renderer. |
| [WebViewRenderProcessClient](https://developer.android.com/reference/kotlin/android/webkit/WebViewRenderProcessClient) | Used to receive callbacks on [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView) renderer events. |

## Annotations

| [JavascriptInterface](https://developer.android.com/reference/kotlin/android/webkit/JavascriptInterface) | Annotation that allows exposing methods to JavaScript. |
