# WebViewClient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebViewClient

Kotlin| [Java](../android/webkit/WebViewClient.md) 
| --- | --- |

```
open class WebViewClient
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.WebViewClient](../android/webkit/WebViewClient.md) |

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_AUTHENTICATION](../android/webkit/WebViewClient.md) User authentication failed on server |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BAD_URL](../android/webkit/WebViewClient.md) Malformed URL |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CONNECT](../android/webkit/WebViewClient.md) Failed to connect to the server |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_FAILED_SSL_HANDSHAKE](../android/webkit/WebViewClient.md) Failed to perform SSL handshake |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_FILE](../android/webkit/WebViewClient.md) Generic file error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_FILE_NOT_FOUND](../android/webkit/WebViewClient.md) File not found |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_HOST_LOOKUP](../android/webkit/WebViewClient.md) Server or proxy hostname lookup failed |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_IO](../android/webkit/WebViewClient.md) Failed to read or write to the server |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PROXY_AUTHENTICATION](../android/webkit/WebViewClient.md) User authentication failed on proxy |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_REDIRECT_LOOP](../android/webkit/WebViewClient.md) Too many redirects |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TIMEOUT](../android/webkit/WebViewClient.md) Connection timed out |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TOO_MANY_REQUESTS](../android/webkit/WebViewClient.md) Too many requests during this load |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNKNOWN](../android/webkit/WebViewClient.md) Generic error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNSAFE_RESOURCE](../android/webkit/WebViewClient.md) Resource load was canceled by Safe Browsing |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNSUPPORTED_AUTH_SCHEME](../android/webkit/WebViewClient.md) Unsupported authentication scheme (not basic or digest) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNSUPPORTED_SCHEME](../android/webkit/WebViewClient.md) Unsupported URI scheme |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAFE_BROWSING_THREAT_BILLING](../android/webkit/WebViewClient.md) The resource was blocked because it may trick the user into a billing agreement. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAFE_BROWSING_THREAT_MALWARE](../android/webkit/WebViewClient.md) The resource was blocked because it contains malware. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAFE_BROWSING_THREAT_PHISHING](../android/webkit/WebViewClient.md) The resource was blocked because it contains deceptive content. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAFE_BROWSING_THREAT_UNKNOWN](../android/webkit/WebViewClient.md) The resource was blocked for an unknown reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAFE_BROWSING_THREAT_UNWANTED_SOFTWARE](../android/webkit/WebViewClient.md) The resource was blocked because it contains unwanted software. |
| --- | --- |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------|---|
| [WebViewClient](../android/webkit/WebViewClient.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [doUpdateVisitedHistory](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `isReload:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notify the host application to update its visited links database. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFormResubmission](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `dontResend:` ` [Message](../android/os/Message.md)!`, `resend:` ` [Message](../android/os/Message.md)!`)` As the host application if the browser should resend data as the requested page was a result of a POST. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLoadResource](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Notify the host application that the WebView will load the resource specified by the given url. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPageCommitVisible](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Notify the host application that [android.webkit.WebView](../android/webkit/WebView.md) content left over from previous page navigations will no longer be drawn. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPageFinished](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Notify the host application that a page has finished loading. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPageStarted](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `favicon:` ` [Bitmap](../android/graphics/Bitmap.md)!`)` Notify the host application that a page has started loading. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceivedClientCertRequest](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `request:` ` [ClientCertRequest](../android/webkit/ClientCertRequest.md)!`)` Notify the host application to handle a SSL client certificate request. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceivedError](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `request:` ` [WebResourceRequest](../android/webkit/WebResourceRequest.md)!`, `error:` ` [WebResourceError](../android/webkit/WebResourceError.md)!`)` Report web resource loading error to the host application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceivedError](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `description:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `failingUrl:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Report an error to the host application. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceivedHttpAuthRequest](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `handler:` ` [HttpAuthHandler](../android/webkit/HttpAuthHandler.md)!`, `host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `realm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Notifies the host application that the WebView received an HTTP authentication request. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceivedHttpError](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `request:` ` [WebResourceRequest](../android/webkit/WebResourceRequest.md)!`, `errorResponse:` ` [WebResourceResponse](../android/webkit/WebResourceResponse.md)!`)` Notify the host application that an HTTP error has been received from the server while loading a resource. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceivedLoginRequest](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `realm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `account:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `args:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Notify the host application that a request to automatically log in the user has been processed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceivedSslError](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `handler:` ` [SslErrorHandler](../android/webkit/SslErrorHandler.md)!`, `error:` ` [SslError](../android/net/http/SslError.md)!`)` Notifies the host application that an SSL error occurred while loading a resource. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onRenderProcessGone](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `detail:` ` [RenderProcessGoneDetail](../android/webkit/RenderProcessGoneDetail.md)!`)` Notify host application that the given WebView's render process has exited. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSafeBrowsingHit](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `request:` ` [WebResourceRequest](../android/webkit/WebResourceRequest.md)!`, `threatType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `callback:` ` [SafeBrowsingResponse](../android/webkit/SafeBrowsingResponse.md)!`)` Notify the host application that a loading URL has been flagged by Safe Browsing. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScaleChanged](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `oldScale:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `newScale:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Notify the host application that the scale applied to the WebView has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTooManyRedirects](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `cancelMsg:` ` [Message](../android/os/Message.md)!`, `continueMsg:` ` [Message](../android/os/Message.md)!`)` Notify the host application that there have been an excessive number of HTTP redirects. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUnhandledKeyEvent](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` Notify the host application that a key was not handled by the WebView. |
| --- | --- |
| open [WebResourceResponse](../android/webkit/WebResourceResponse.md)? | [shouldInterceptRequest](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `request:` ` [WebResourceRequest](../android/webkit/WebResourceRequest.md)!`)` Notify the host application of a resource request and allow the application to return the data. |
| open [WebResourceResponse](../android/webkit/WebResourceResponse.md)? | [shouldInterceptRequest](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Notify the host application of a resource request and allow the application to return the data. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldOverrideKeyEvent](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` Give the host application a chance to handle the key event synchronously. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldOverrideUrlLoading](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `request:` ` [WebResourceRequest](../android/webkit/WebResourceRequest.md)!`)` Give the host application a chance to take control when a URL is about to be loaded in the current WebView. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldOverrideUrlLoading](../android/webkit/WebViewClient.md))`(`view:` ` [WebView](../android/webkit/WebView.md)!`, `url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Give the host application a chance to take control when a URL is about to be loaded in the current WebView. |

## Constants

### ERROR_AUTHENTICATION

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_AUTHENTICATION: Int
```

User authentication failed on server 

 Value: -4

### ERROR_BAD_URL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_BAD_URL: Int
```

Malformed URL 

 Value: -12

### ERROR_CONNECT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_CONNECT: Int
```

Failed to connect to the server 

 Value: -6

### ERROR_FAILED_SSL_HANDSHAKE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_FAILED_SSL_HANDSHAKE: Int
```

Failed to perform SSL handshake 

 Value: -11

### ERROR_FILE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_FILE: Int
```

Generic file error 

 Value: -13

### ERROR_FILE_NOT_FOUND

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_FILE_NOT_FOUND: Int
```

File not found 

 Value: -14

### ERROR_HOST_LOOKUP

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_HOST_LOOKUP: Int
```

Server or proxy hostname lookup failed 

 Value: -2

### ERROR_IO

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_IO: Int
```

Failed to read or write to the server 

 Value: -7

### ERROR_PROXY_AUTHENTICATION

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PROXY_AUTHENTICATION: Int
```

User authentication failed on proxy 

 Value: -5

### ERROR_REDIRECT_LOOP

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_REDIRECT_LOOP: Int
```

Too many redirects 

 Value: -9

### ERROR_TIMEOUT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TIMEOUT: Int
```

Connection timed out 

 Value: -8

### ERROR_TOO_MANY_REQUESTS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TOO_MANY_REQUESTS: Int
```

Too many requests during this load 

 Value: -15

### ERROR_UNKNOWN

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNKNOWN: Int
```

Generic error 

 Value: -1

### ERROR_UNSAFE_RESOURCE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNSAFE_RESOURCE: Int
```

Resource load was canceled by Safe Browsing 

 Value: -16

### ERROR_UNSUPPORTED_AUTH_SCHEME

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNSUPPORTED_AUTH_SCHEME: Int
```

Unsupported authentication scheme (not basic or digest) 

 Value: -3

### ERROR_UNSUPPORTED_SCHEME

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNSUPPORTED_SCHEME: Int
```

Unsupported URI scheme 

 Value: -10

### SAFE_BROWSING_THREAT_BILLING

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAFE_BROWSING_THREAT_BILLING: Int
```

The resource was blocked because it may trick the user into a billing agreement.

This constant is only used when targetSdkVersion is at least [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md). Otherwise, [SAFE_BROWSING_THREAT_UNKNOWN](../android/webkit/WebViewClient.md) is used instead. 

 Value: 4

### SAFE_BROWSING_THREAT_MALWARE

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAFE_BROWSING_THREAT_MALWARE: Int
```

The resource was blocked because it contains malware. 

 Value: 1

### SAFE_BROWSING_THREAT_PHISHING

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAFE_BROWSING_THREAT_PHISHING: Int
```

The resource was blocked because it contains deceptive content. 

 Value: 2

### SAFE_BROWSING_THREAT_UNKNOWN

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAFE_BROWSING_THREAT_UNKNOWN: Int
```

The resource was blocked for an unknown reason. 

 Value: 0

### SAFE_BROWSING_THREAT_UNWANTED_SOFTWARE

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAFE_BROWSING_THREAT_UNWANTED_SOFTWARE: Int
```

The resource was blocked because it contains unwanted software. 

 Value: 3

## Public constructors

### WebViewClient

```
WebViewClient()
```

## Public methods

### doUpdateVisitedHistory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun doUpdateVisitedHistory(
    view: WebView!, 
    url: String!, 
    isReload: Boolean
): Unit
```

Notify the host application to update its visited links database.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView that is initiating the callback. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The url being visited. |
| `isReload` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if this url is being reloaded. |
| --- | --- |

### onFormResubmission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onFormResubmission(
    view: WebView!, 
    dontResend: Message!, 
    resend: Message!
): Unit
```

As the host application if the browser should resend data as the requested page was a result of a POST. The default is to not resend the data.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView that is initiating the callback. |
| `dontResend` | [Message](../android/os/Message.md)!:The message to send if the browser should not resend |
| `resend` | [Message](../android/os/Message.md)!:The message to send if the browser should resend data |
| --- | --- |

### onLoadResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onLoadResource(
    view: WebView!, 
    url: String!
): Unit
```

Notify the host application that the WebView will load the resource specified by the given url.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView that is initiating the callback. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The url of the resource the WebView will load. |

### onPageCommitVisible

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPageCommitVisible(
    view: WebView!, 
    url: String!
): Unit
```

Notify the host application that [android.webkit.WebView](../android/webkit/WebView.md) content left over from previous page navigations will no longer be drawn.

This callback can be used to determine the point at which it is safe to make a recycled [android.webkit.WebView](../android/webkit/WebView.md) visible, ensuring that no stale content is shown. It is called at the earliest point at which it can be guaranteed that [WebView.onDraw](../android/webkit/WebView.md))will no longer draw any content from previous navigations. The next draw will display either the [background color](../android/webkit/WebView.md))of the [WebView](../android/webkit/WebView.md), or some of the contents of the newly loaded page.

This method is called when the body of the HTTP response has started loading, is reflected in the DOM, and will be visible in subsequent draws. This callback occurs early in the document loading process, and as such you should expect that linked resources (for example, CSS and images) may not be available.

For more fine-grained notification of visual state updates, see [android.webkit.WebView#postVisualStateCallback](../android/webkit/WebView.md)).

Please note that all the conditions and recommendations applicable to [WebView.postVisualStateCallback](../android/webkit/WebView.md))also apply to this API.

This callback is only called for main frame navigations.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The [android.webkit.WebView](../android/webkit/WebView.md) for which the navigation occurred. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The URL corresponding to the page navigation that triggered this callback. |

### onPageFinished

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPageFinished(
    view: WebView!, 
    url: String!
): Unit
```

Notify the host application that a page has finished loading. This method is called only for main frame. Receiving an`onPageFinished()`callback does not guarantee that the next frame drawn by WebView will reflect the state of the DOM at this point. In order to be notified that the current DOM state is ready to be rendered, request a visual state callback with [WebView.postVisualStateCallback](../android/webkit/WebView.md))and wait for the supplied callback to be triggered.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView that is initiating the callback. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The url of the page. |

### onPageStarted

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPageStarted(
    view: WebView!, 
    url: String!, 
    favicon: Bitmap!
): Unit
```

Notify the host application that a page has started loading. This method is called once for each main frame load so a page with iframes or framesets will call onPageStarted one time for the main frame. This also means that onPageStarted will not be called when the contents of an embedded frame changes, i.e. clicking a link whose target is an iframe, it will also not be called for fragment navigations (navigations to #fragment_id).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView that is initiating the callback. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The url to be loaded. |
| `favicon` | [Bitmap](../android/graphics/Bitmap.md)!:The favicon for this page if it already exists in the database. |
| --- | --- |

### onReceivedClientCertRequest

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onReceivedClientCertRequest(
    view: WebView!, 
    request: ClientCertRequest!
): Unit
```

Notify the host application to handle a SSL client certificate request. The host application is responsible for showing the UI if desired and providing the keys. There are three ways to respond: [ClientCertRequest.proceed](../android/webkit/ClientCertRequest.md)), [ClientCertRequest.cancel](../android/webkit/ClientCertRequest.md)), or [android.webkit.ClientCertRequest#ignore](../android/webkit/ClientCertRequest.md)). Webview stores the response in memory (for the life of the application) if [ClientCertRequest.proceed](../android/webkit/ClientCertRequest.md))or [ClientCertRequest.cancel](../android/webkit/ClientCertRequest.md))is called and does not call`onReceivedClientCertRequest()`again for the same host and port pair. Webview does not store the response if [ClientCertRequest.ignore](../android/webkit/ClientCertRequest.md))is called. Note that, multiple layers in chromium network stack might be caching the responses, so the behavior for ignore is only a best case effort. This method is called on the UI thread. During the callback, the connection is suspended. For most use cases, the application program should implement the [android.security.KeyChainAliasCallback](../android/security/KeyChainAliasCallback.md) interface and pass it to android.security.KeyChain#choosePrivateKeyAlias to start an activity for the user to choose the proper alias. The keychain activity will provide the alias through the callback method in the implemented interface. Next the application should create an async task to call [android.security.KeyChain#getPrivateKey](../android/security/KeyChain.md))to receive the key. An example implementation of client certificates can be seen at [AOSP Browser](https://android.googlesource.com/platform/packages/apps/Browser/+/android-5.1.1_r1/src/com/android/browser/Tab.java) The default behavior is to cancel, returning no client certificate.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView that is initiating the callback |
| `request` | [ClientCertRequest](../android/webkit/ClientCertRequest.md)!:An instance of a [ClientCertRequest](../android/webkit/ClientCertRequest.md) |

### onReceivedError

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onReceivedError(
    view: WebView!, 
    request: WebResourceRequest!, 
    error: WebResourceError!
): Unit
```

Report web resource loading error to the host application. These errors usually indicate inability to connect to the server. Note that unlike the deprecated version of the callback, the new version will be called for any resource (iframe, image, etc.), not just for the main page. Thus, it is recommended to perform minimum required work in this callback.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView that is initiating the callback. |
| `request` | [WebResourceRequest](../android/webkit/WebResourceRequest.md)!:The originating request. |
| `error` | [WebResourceError](../android/webkit/WebResourceError.md)!:Information about the error occurred. |
| --- | --- |

### onReceivedError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onReceivedError(
    view: WebView!, 
    errorCode: Int, 
    description: String!, 
    failingUrl: String!
): Unit
```

**Deprecated:** *Use [onReceivedError(WebView, WebResourceRequest, WebResourceError)](../android/webkit/WebViewClient.md))on [android.os.Build.VERSION_CODES#M](../android/os/Build.VERSION_CODES.md) and above.*

Report an error to the host application. These errors are unrecoverable (i.e. the main resource is unavailable). The`errorCode`parameter corresponds to one of the`ERROR_*`constants.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView that is initiating the callback. |
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The error code corresponding to an ERROR_\* value. |
| `description` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A String describing the error. |
| --- | --- |
| `failingUrl` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The url that failed to load. |

### onReceivedHttpAuthRequest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onReceivedHttpAuthRequest(
    view: WebView!, 
    handler: HttpAuthHandler!, 
    host: String!, 
    realm: String!
): Unit
```

Notifies the host application that the WebView received an HTTP authentication request. The host application can use the supplied [HttpAuthHandler](../android/webkit/HttpAuthHandler.md) to set the WebView's response to the request. The default behavior is to cancel the request.

**Note:**The supplied HttpAuthHandler must be used on the UI thread.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:the WebView that is initiating the callback |
| `handler` | [HttpAuthHandler](../android/webkit/HttpAuthHandler.md)!:the HttpAuthHandler used to set the WebView's response |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the host requiring authentication |
| --- | --- |
| `realm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the realm for which authentication is required |

**See Also**

- [android.webkit.WebView#getHttpAuthUsernamePassword](../android/webkit/WebView.md)) 

### onReceivedHttpError

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onReceivedHttpError(
    view: WebView!, 
    request: WebResourceRequest!, 
    errorResponse: WebResourceResponse!
): Unit
```

Notify the host application that an HTTP error has been received from the server while loading a resource. HTTP errors have status codes \>= 400. This callback will be called for any resource (iframe, image, etc.), not just for the main page. Thus, it is recommended to perform minimum required work in this callback. Note that the content of the server response may not be provided within the`errorResponse`parameter.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView that is initiating the callback. |
| `request` | [WebResourceRequest](../android/webkit/WebResourceRequest.md)!:The originating request. |
| `errorResponse` | [WebResourceResponse](../android/webkit/WebResourceResponse.md)!:Information about the error occurred. |
| --- | --- |

### onReceivedLoginRequest

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onReceivedLoginRequest(
    view: WebView!, 
    realm: String!, 
    account: String?, 
    args: String!
): Unit
```

Notify the host application that a request to automatically log in the user has been processed.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView requesting the login. |
| `realm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The account realm used to look up accounts. |
| `account` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:An optional account. If not`null`, the account should be checked against accounts on the device. If it is a valid account, it should be used to log in the user. |
| --- | --- |
| `args` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Authenticator specific arguments used to log in the user. |

### onReceivedSslError

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onReceivedSslError(
    view: WebView!, 
    handler: SslErrorHandler!, 
    error: SslError!
): Unit
```

Notifies the host application that an SSL error occurred while loading a resource. The host application must call either [SslErrorHandler.cancel()](../android/webkit/SslErrorHandler.md))or [SslErrorHandler.proceed()](../android/webkit/SslErrorHandler.md)).

**Warning:** Application overrides of this method can be used to display custom error pages or to silently log issues, but the host application should always call`SslErrorHandler#cancel()`and never proceed past errors.

**Note:** Do not prompt the user about SSL errors. Users are unlikely to be able to make an informed security decision, and`WebView`does not provide a UI for showing the details of the error in a meaningful way.

The decision to call`proceed()`or`cancel()`may be retained to facilitate responses to future SSL errors. The default behavior is to cancel the resource loading process.

This API is called only for recoverable SSL certificate errors. For non-recoverable errors (such as when the server fails the client), the`WebView`calls [onReceivedError(WebView,](../android/webkit/WebViewClient.md))with the [ERROR_FAILED_SSL_HANDSHAKE](../android/webkit/WebViewClient.md) argument.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:`WebView`that initiated the callback. |
| `handler` | [SslErrorHandler](../android/webkit/SslErrorHandler.md)!: [SslErrorHandler](../android/webkit/SslErrorHandler.md) that handles the user's response. |
| `error` | [SslError](../android/net/http/SslError.md)!:SSL error object. |
| --- | --- |

### onRenderProcessGone

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRenderProcessGone(
    view: WebView!, 
    detail: RenderProcessGoneDetail!
): Boolean
```

Notify host application that the given WebView's render process has exited. Multiple WebView instances may be associated with a single render process; onRenderProcessGone will be called for each WebView that was affected. The application's implementation of this callback should only attempt to clean up the specific WebView given as a parameter, and should not assume that other WebView instances are affected. The given WebView can't be used, and should be removed from the view hierarchy, all references to it should be cleaned up, e.g any references in the Activity or other classes saved using [android.view.View#findViewById](../android/view/View.md))and similar calls, etc. To cause an render process crash for test purpose, the application can call`loadUrl("chrome://crash")`on the WebView. Note that multiple WebView instances may be affected if they share a render process, not just the specific WebView which loaded chrome://crash.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView which needs to be cleaned up. |
| `detail` | [RenderProcessGoneDetail](../android/webkit/RenderProcessGoneDetail.md)!:the reason why it exited. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the host application handled the situation that process has exited, otherwise, application will crash if render process crashed, or be killed if render process was killed by the system. |

### onSafeBrowsingHit

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSafeBrowsingHit(
    view: WebView!, 
    request: WebResourceRequest!, 
    threatType: Int, 
    callback: SafeBrowsingResponse!
): Unit
```

Notify the host application that a loading URL has been flagged by Safe Browsing. The application must invoke the callback to indicate the preferred response. The default behavior is to show an interstitial to the user, with the reporting checkbox visible. If the application needs to show its own custom interstitial UI, the callback can be invoked asynchronously with [SafeBrowsingResponse.backToSafety](../android/webkit/SafeBrowsingResponse.md))or [android.webkit.SafeBrowsingResponse#proceed](../android/webkit/SafeBrowsingResponse.md)), depending on user response.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView that hit the malicious resource. |
| `request` | [WebResourceRequest](../android/webkit/WebResourceRequest.md)!:Object containing the details of the request. |
| `threatType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The reason the resource was caught by Safe Browsing, corresponding to a`SAFE_BROWSING_THREAT_*`value. Value is [android.webkit.WebViewClient#SAFE_BROWSING_THREAT_UNKNOWN](../android/webkit/WebViewClient.md), [android.webkit.WebViewClient#SAFE_BROWSING_THREAT_MALWARE](../android/webkit/WebViewClient.md), [android.webkit.WebViewClient#SAFE_BROWSING_THREAT_PHISHING](../android/webkit/WebViewClient.md), [android.webkit.WebViewClient#SAFE_BROWSING_THREAT_UNWANTED_SOFTWARE](../android/webkit/WebViewClient.md), or [android.webkit.WebViewClient#SAFE_BROWSING_THREAT_BILLING](../android/webkit/WebViewClient.md) |
| --- | --- |
| `callback` | [SafeBrowsingResponse](../android/webkit/SafeBrowsingResponse.md)!:Applications must invoke one of the callback methods. |

### onScaleChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onScaleChanged(
    view: WebView!, 
    oldScale: Float, 
    newScale: Float
): Unit
```

Notify the host application that the scale applied to the WebView has changed.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView that is initiating the callback. |
| `oldScale` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The old scale factor |
| `newScale` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The new scale factor |
| --- | --- |

### onTooManyRedirects

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTooManyRedirects(
    view: WebView!, 
    cancelMsg: Message!, 
    continueMsg: Message!
): Unit
```

**Deprecated:** *This method is no longer called. When the WebView encounters a redirect loop, it will cancel the load.*

Notify the host application that there have been an excessive number of HTTP redirects. As the host application if it would like to continue trying to load the resource. The default behavior is to send the cancel message.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView that is initiating the callback. |
| `cancelMsg` | [Message](../android/os/Message.md)!:The message to send if the host wants to cancel |
| `continueMsg` | [Message](../android/os/Message.md)!:The message to send if the host wants to continue |
| --- | --- |

### onUnhandledKeyEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onUnhandledKeyEvent(
    view: WebView!, 
    event: KeyEvent!
): Unit
```

Notify the host application that a key was not handled by the WebView. Except system keys, WebView always consumes the keys in the normal flow or if [shouldOverrideKeyEvent](../android/webkit/WebViewClient.md))returns`true`. This is called asynchronously from where the key is dispatched. It gives the host application a chance to handle the unhandled key events.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView that is initiating the callback. |
| `event` | [KeyEvent](../android/view/KeyEvent.md)!:The key event. |

### shouldInterceptRequest

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shouldInterceptRequest(
    view: WebView!, 
    request: WebResourceRequest!
): WebResourceResponse?
```

Notify the host application of a resource request and allow the application to return the data. If the return value is`null`, the WebView will continue to load the resource as usual. Otherwise, the return response and data will be used.

This callback is invoked for a variety of URL schemes (e.g.,`http(s):`,`data:`,`file:`, etc.), not only those schemes which send requests over the network. This is not called for`javascript:`URLs,`blob:`URLs, or for assets accessed via`file:///android_asset/`or`file:///android_res/`URLs.

In the case of redirects, this is only called for the initial resource URL, not any subsequent redirect URLs.

**Note:**This method is called on a thread other than the UI thread so clients should exercise caution when accessing private data or the view system.

**Note:** When Safe Browsing is enabled, these URLs still undergo Safe Browsing checks. If this is undesired, you can use [WebView.setSafeBrowsingWhitelist](../android/webkit/WebView.md))to skip Safe Browsing checks for that host or dismiss the warning in [onSafeBrowsingHit](../android/webkit/WebViewClient.md))by calling [SafeBrowsingResponse.proceed](../android/webkit/SafeBrowsingResponse.md)).

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The [android.webkit.WebView](../android/webkit/WebView.md) that is requesting the resource. |
| `request` | [WebResourceRequest](../android/webkit/WebResourceRequest.md)!:Object containing the details of the request. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WebResourceResponse](../android/webkit/WebResourceResponse.md)? | A [android.webkit.WebResourceResponse](../android/webkit/WebResourceResponse.md) containing the response information or`null`if the WebView should load the resource itself. |

### shouldInterceptRequest

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shouldInterceptRequest(
    view: WebView!, 
    url: String!
): WebResourceResponse?
```

**Deprecated:** *Use [shouldInterceptRequest(WebView, WebResourceRequest)](../android/webkit/WebViewClient.md))on [android.os.Build.VERSION_CODES#M](../android/os/Build.VERSION_CODES.md) and above.*

Notify the host application of a resource request and allow the application to return the data. If the return value is`null`, the WebView will continue to load the resource as usual. Otherwise, the return response and data will be used.

This callback is invoked for a variety of URL schemes (e.g.,`http(s):`,`data:`,`file:`, etc.), not only those schemes which send requests over the network. This is not called for`javascript:`URLs,`blob:`URLs, or for assets accessed via`file:///android_asset/`or`file:///android_res/`URLs.

In the case of redirects, this is only called for the initial resource URL, not any subsequent redirect URLs.

**Note:**This method is called on a thread other than the UI thread so clients should exercise caution when accessing private data or the view system.

**Note:** When Safe Browsing is enabled, these URLs still undergo Safe Browsing checks. If this is undesired, you can use [WebView.setSafeBrowsingWhitelist](../android/webkit/WebView.md))to skip Safe Browsing checks for that host or dismiss the warning in [onSafeBrowsingHit](../android/webkit/WebViewClient.md))by calling [SafeBrowsingResponse.proceed](../android/webkit/SafeBrowsingResponse.md)).

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The [android.webkit.WebView](../android/webkit/WebView.md) that is requesting the resource. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The raw url of the resource. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WebResourceResponse](../android/webkit/WebResourceResponse.md)? | A [android.webkit.WebResourceResponse](../android/webkit/WebResourceResponse.md) containing the response information or`null`if the WebView should load the resource itself. |

### shouldOverrideKeyEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shouldOverrideKeyEvent(
    view: WebView!, 
    event: KeyEvent!
): Boolean
```

Give the host application a chance to handle the key event synchronously. e.g. menu shortcut key events need to be filtered this way. If return true, WebView will not handle the key event. If return`false`, WebView will always handle the key event, so none of the super in the view chain will see the key event. The default behavior returns`false`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView that is initiating the callback. |
| `event` | [KeyEvent](../android/view/KeyEvent.md)!:The key event. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the host application wants to handle the key event itself, otherwise return`false` |

### shouldOverrideUrlLoading

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shouldOverrideUrlLoading(
    view: WebView!, 
    request: WebResourceRequest!
): Boolean
```

Give the host application a chance to take control when a URL is about to be loaded in the current WebView. If a WebViewClient is not provided, by default WebView will ask Activity Manager to choose the proper handler for the URL. If a WebViewClient is provided, returning`true`causes the current WebView to abort loading the URL, while returning`false`causes the WebView to continue loading the URL as usual.

This callback is not called for all page navigations. In particular, this is not called for navigations which the app initiated with`loadUrl()`: this callback would not serve a purpose in this case, because the app already knows about the navigation. This callback lets the app know about navigations initiated by the web page (such as navigations initiated by JavaScript code), by the user (such as when the user taps on a link), or by an HTTP redirect (ex. if`loadUrl("foo.com")`redirects to`"bar.com"`because of HTTP 301).

**Note:** Do not call [WebView.loadUrl(String)](../android/webkit/WebView.md))with the request's URL and then return`true`. This unnecessarily cancels the current load and starts a new load with the same URL. The correct way to continue loading a given URL is to simply return`false`, without calling [WebView.loadUrl(String)](../android/webkit/WebView.md)).

**Note:**This method is not called for POST requests.

**Note:** This method may be called for subframes and with non-HTTP(S) schemes; calling [WebView.loadUrl(String)](../android/webkit/WebView.md))with such a URL will fail.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView that is initiating the callback. |
| `request` | [WebResourceRequest](../android/webkit/WebResourceRequest.md)!:Object containing the details of the request. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`to cancel the current load, otherwise return`false`. |

### shouldOverrideUrlLoading

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shouldOverrideUrlLoading(
    view: WebView!, 
    url: String!
): Boolean
```

**Deprecated:** *Use [shouldOverrideUrlLoading(WebView, WebResourceRequest)](../android/webkit/WebViewClient.md))on [android.os.Build.VERSION_CODES#N](../android/os/Build.VERSION_CODES.md) and above.*

Give the host application a chance to take control when a URL is about to be loaded in the current WebView. If a WebViewClient is not provided, by default WebView will ask Activity Manager to choose the proper handler for the URL. If a WebViewClient is provided, returning`true`causes the current WebView to abort loading the URL, while returning`false`causes the WebView to continue loading the URL as usual.

**Note:** Do not call [WebView.loadUrl(String)](../android/webkit/WebView.md))with the same URL and then return`true`. This unnecessarily cancels the current load and starts a new load with the same URL. The correct way to continue loading a given URL is to simply return`false`, without calling [WebView.loadUrl(String)](../android/webkit/WebView.md)).

**Note:**This method is not called for POST requests.

**Note:** This method may be called for subframes and with non-HTTP(S) schemes; calling [WebView.loadUrl(String)](../android/webkit/WebView.md))with such a URL will fail.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](../android/webkit/WebView.md)!:The WebView that is initiating the callback. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The URL to be loaded. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`to cancel the current load, otherwise return`false`. |
