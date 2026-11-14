# WebViewClient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebViewClient

Kotlin| [Java](https://developer.android.com/reference/android/webkit/WebViewClient "View this page in Java") 

```
open class WebViewClient
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.webkit.WebViewClient](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#) |

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_AUTHENTICATION](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#ERROR_AUTHENTICATION:kotlin.Int) User authentication failed on server |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BAD_URL](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#ERROR_BAD_URL:kotlin.Int) Malformed URL |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_CONNECT](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#ERROR_CONNECT:kotlin.Int) Failed to connect to the server |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_FAILED_SSL_HANDSHAKE](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#ERROR_FAILED_SSL_HANDSHAKE:kotlin.Int) Failed to perform SSL handshake |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_FILE](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#ERROR_FILE:kotlin.Int) Generic file error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_FILE_NOT_FOUND](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#ERROR_FILE_NOT_FOUND:kotlin.Int) File not found |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_HOST_LOOKUP](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#ERROR_HOST_LOOKUP:kotlin.Int) Server or proxy hostname lookup failed |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_IO](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#ERROR_IO:kotlin.Int) Failed to read or write to the server |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PROXY_AUTHENTICATION](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#ERROR_PROXY_AUTHENTICATION:kotlin.Int) User authentication failed on proxy |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_REDIRECT_LOOP](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#ERROR_REDIRECT_LOOP:kotlin.Int) Too many redirects |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TIMEOUT](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#ERROR_TIMEOUT:kotlin.Int) Connection timed out |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TOO_MANY_REQUESTS](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#ERROR_TOO_MANY_REQUESTS:kotlin.Int) Too many requests during this load |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNKNOWN](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#ERROR_UNKNOWN:kotlin.Int) Generic error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNSAFE_RESOURCE](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#ERROR_UNSAFE_RESOURCE:kotlin.Int) Resource load was canceled by Safe Browsing |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNSUPPORTED_AUTH_SCHEME](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#ERROR_UNSUPPORTED_AUTH_SCHEME:kotlin.Int) Unsupported authentication scheme (not basic or digest) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNSUPPORTED_SCHEME](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#ERROR_UNSUPPORTED_SCHEME:kotlin.Int) Unsupported URI scheme |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAFE_BROWSING_THREAT_BILLING](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#SAFE_BROWSING_THREAT_BILLING:kotlin.Int) The resource was blocked because it may trick the user into a billing agreement. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAFE_BROWSING_THREAT_MALWARE](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#SAFE_BROWSING_THREAT_MALWARE:kotlin.Int) The resource was blocked because it contains malware. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAFE_BROWSING_THREAT_PHISHING](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#SAFE_BROWSING_THREAT_PHISHING:kotlin.Int) The resource was blocked because it contains deceptive content. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAFE_BROWSING_THREAT_UNKNOWN](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#SAFE_BROWSING_THREAT_UNKNOWN:kotlin.Int) The resource was blocked for an unknown reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAFE_BROWSING_THREAT_UNWANTED_SOFTWARE](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#SAFE_BROWSING_THREAT_UNWANTED_SOFTWARE:kotlin.Int) The resource was blocked because it contains unwanted software. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------|---|
| [WebViewClient](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#WebViewClient())`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [doUpdateVisitedHistory](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#doUpdateVisitedHistory(android.webkit.WebView,%20kotlin.String,%20kotlin.Boolean))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `isReload:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notify the host application to update its visited links database. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFormResubmission](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onFormResubmission(android.webkit.WebView,%20android.os.Message,%20android.os.Message))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `dontResend:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)!`, `resend:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)!`)` As the host application if the browser should resend data as the requested page was a result of a POST. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onLoadResource](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onLoadResource(android.webkit.WebView,%20kotlin.String))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Notify the host application that the WebView will load the resource specified by the given url. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPageCommitVisible](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onPageCommitVisible(android.webkit.WebView,%20kotlin.String))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Notify the host application that [android.webkit.WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView) content left over from previous page navigations will no longer be drawn. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPageFinished](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onPageFinished(android.webkit.WebView,%20kotlin.String))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Notify the host application that a page has finished loading. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPageStarted](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onPageStarted(android.webkit.WebView,%20kotlin.String,%20android.graphics.Bitmap))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `favicon:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!`)` Notify the host application that a page has started loading. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceivedClientCertRequest](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onReceivedClientCertRequest(android.webkit.WebView,%20android.webkit.ClientCertRequest))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `request:` ` [ClientCertRequest](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest)!`)` Notify the host application to handle a SSL client certificate request. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceivedError](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onReceivedError(android.webkit.WebView,%20android.webkit.WebResourceRequest,%20android.webkit.WebResourceError))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `request:` ` [WebResourceRequest](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest)!`, `error:` ` [WebResourceError](https://developer.android.com/reference/kotlin/android/webkit/WebResourceError)!`)` Report web resource loading error to the host application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceivedError](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onReceivedError(android.webkit.WebView,%20kotlin.Int,%20kotlin.String,%20kotlin.String))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `description:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `failingUrl:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Report an error to the host application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceivedHttpAuthRequest](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onReceivedHttpAuthRequest(android.webkit.WebView,%20android.webkit.HttpAuthHandler,%20kotlin.String,%20kotlin.String))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `handler:` ` [HttpAuthHandler](https://developer.android.com/reference/kotlin/android/webkit/HttpAuthHandler)!`, `host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `realm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Notifies the host application that the WebView received an HTTP authentication request. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceivedHttpError](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onReceivedHttpError(android.webkit.WebView,%20android.webkit.WebResourceRequest,%20android.webkit.WebResourceResponse))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `request:` ` [WebResourceRequest](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest)!`, `errorResponse:` ` [WebResourceResponse](https://developer.android.com/reference/kotlin/android/webkit/WebResourceResponse)!`)` Notify the host application that an HTTP error has been received from the server while loading a resource. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceivedLoginRequest](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onReceivedLoginRequest(android.webkit.WebView,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `realm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `account:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `args:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Notify the host application that a request to automatically log in the user has been processed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceivedSslError](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onReceivedSslError(android.webkit.WebView,%20android.webkit.SslErrorHandler,%20android.net.http.SslError))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `handler:` ` [SslErrorHandler](https://developer.android.com/reference/kotlin/android/webkit/SslErrorHandler)!`, `error:` ` [SslError](https://developer.android.com/reference/kotlin/android/net/http/SslError.html#)!`)` Notifies the host application that an SSL error occurred while loading a resource. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onRenderProcessGone](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onRenderProcessGone(android.webkit.WebView,%20android.webkit.RenderProcessGoneDetail))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `detail:` ` [RenderProcessGoneDetail](https://developer.android.com/reference/kotlin/android/webkit/RenderProcessGoneDetail)!`)` Notify host application that the given WebView's render process has exited. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSafeBrowsingHit](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onSafeBrowsingHit(android.webkit.WebView,%20android.webkit.WebResourceRequest,%20kotlin.Int,%20android.webkit.SafeBrowsingResponse))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `request:` ` [WebResourceRequest](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest)!`, `threatType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `callback:` ` [SafeBrowsingResponse](https://developer.android.com/reference/kotlin/android/webkit/SafeBrowsingResponse)!`)` Notify the host application that a loading URL has been flagged by Safe Browsing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScaleChanged](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onScaleChanged(android.webkit.WebView,%20kotlin.Float,%20kotlin.Float))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `oldScale:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `newScale:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Notify the host application that the scale applied to the WebView has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTooManyRedirects](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onTooManyRedirects(android.webkit.WebView,%20android.os.Message,%20android.os.Message))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `cancelMsg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)!`, `continueMsg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)!`)` Notify the host application that there have been an excessive number of HTTP redirects. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUnhandledKeyEvent](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onUnhandledKeyEvent(android.webkit.WebView,%20android.view.KeyEvent))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` Notify the host application that a key was not handled by the WebView. |
| open [WebResourceResponse](https://developer.android.com/reference/kotlin/android/webkit/WebResourceResponse)? | [shouldInterceptRequest](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#shouldInterceptRequest(android.webkit.WebView,%20android.webkit.WebResourceRequest))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `request:` ` [WebResourceRequest](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest)!`)` Notify the host application of a resource request and allow the application to return the data. |
| open [WebResourceResponse](https://developer.android.com/reference/kotlin/android/webkit/WebResourceResponse)? | [shouldInterceptRequest](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#shouldInterceptRequest(android.webkit.WebView,%20kotlin.String))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Notify the host application of a resource request and allow the application to return the data. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldOverrideKeyEvent](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#shouldOverrideKeyEvent(android.webkit.WebView,%20android.view.KeyEvent))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` Give the host application a chance to handle the key event synchronously. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldOverrideUrlLoading](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#shouldOverrideUrlLoading(android.webkit.WebView,%20android.webkit.WebResourceRequest))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `request:` ` [WebResourceRequest](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest)!`)` Give the host application a chance to take control when a URL is about to be loaded in the current WebView. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldOverrideUrlLoading](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#shouldOverrideUrlLoading(android.webkit.WebView,%20kotlin.String))`(`view:` ` [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!`, `url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Give the host application a chance to take control when a URL is about to be loaded in the current WebView. |

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

This constant is only used when targetSdkVersion is at least [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int). Otherwise, [SAFE_BROWSING_THREAT_UNKNOWN](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#SAFE_BROWSING_THREAT_UNKNOWN:kotlin.Int) is used instead. 

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
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView that is initiating the callback. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The url being visited. |
| `isReload` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if this url is being reloaded. |

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
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView that is initiating the callback. |
| `dontResend` | [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)!:The message to send if the browser should not resend |
| `resend` | [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)!:The message to send if the browser should resend data |

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
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView that is initiating the callback. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The url of the resource the WebView will load. |

### onPageCommitVisible

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPageCommitVisible(
    view: WebView!, 
    url: String!
): Unit
```

Notify the host application that [android.webkit.WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView) content left over from previous page navigations will no longer be drawn.

This callback can be used to determine the point at which it is safe to make a recycled [android.webkit.WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView) visible, ensuring that no stale content is shown. It is called at the earliest point at which it can be guaranteed that [WebView.onDraw](https://developer.android.com/reference/kotlin/android/webkit/WebView#onDraw(android.graphics.Canvas))will no longer draw any content from previous navigations. The next draw will display either the [background color](https://developer.android.com/reference/kotlin/android/webkit/WebView#setBackgroundColor(kotlin.Int))of the [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView), or some of the contents of the newly loaded page.

This method is called when the body of the HTTP response has started loading, is reflected in the DOM, and will be visible in subsequent draws. This callback occurs early in the document loading process, and as such you should expect that linked resources (for example, CSS and images) may not be available.

For more fine-grained notification of visual state updates, see [android.webkit.WebView#postVisualStateCallback](https://developer.android.com/reference/kotlin/android/webkit/WebView#postVisualStateCallback(kotlin.Long,%20android.webkit.WebView.VisualStateCallback)).

Please note that all the conditions and recommendations applicable to [WebView.postVisualStateCallback](https://developer.android.com/reference/kotlin/android/webkit/WebView#postVisualStateCallback(kotlin.Long,%20android.webkit.WebView.VisualStateCallback))also apply to this API.

This callback is only called for main frame navigations.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The [android.webkit.WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView) for which the navigation occurred. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The URL corresponding to the page navigation that triggered this callback. |

### onPageFinished

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPageFinished(
    view: WebView!, 
    url: String!
): Unit
```

Notify the host application that a page has finished loading. This method is called only for main frame. Receiving an`onPageFinished()`callback does not guarantee that the next frame drawn by WebView will reflect the state of the DOM at this point. In order to be notified that the current DOM state is ready to be rendered, request a visual state callback with [WebView.postVisualStateCallback](https://developer.android.com/reference/kotlin/android/webkit/WebView#postVisualStateCallback(kotlin.Long,%20android.webkit.WebView.VisualStateCallback))and wait for the supplied callback to be triggered.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView that is initiating the callback. |
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
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView that is initiating the callback. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The url to be loaded. |
| `favicon` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!:The favicon for this page if it already exists in the database. |

### onReceivedClientCertRequest

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onReceivedClientCertRequest(
    view: WebView!, 
    request: ClientCertRequest!
): Unit
```

Notify the host application to handle a SSL client certificate request. The host application is responsible for showing the UI if desired and providing the keys. There are three ways to respond: [ClientCertRequest.proceed](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest#proceed(java.security.PrivateKey,%20kotlin.Array)), [ClientCertRequest.cancel](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest#cancel()), or [android.webkit.ClientCertRequest#ignore](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest#ignore()). Webview stores the response in memory (for the life of the application) if [ClientCertRequest.proceed](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest#proceed(java.security.PrivateKey,%20kotlin.Array))or [ClientCertRequest.cancel](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest#cancel())is called and does not call`onReceivedClientCertRequest()`again for the same host and port pair. Webview does not store the response if [ClientCertRequest.ignore](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest#ignore())is called. Note that, multiple layers in chromium network stack might be caching the responses, so the behavior for ignore is only a best case effort. This method is called on the UI thread. During the callback, the connection is suspended. For most use cases, the application program should implement the [android.security.KeyChainAliasCallback](https://developer.android.com/reference/kotlin/android/security/KeyChainAliasCallback.html#) interface and pass it to android.security.KeyChain#choosePrivateKeyAlias to start an activity for the user to choose the proper alias. The keychain activity will provide the alias through the callback method in the implemented interface. Next the application should create an async task to call [android.security.KeyChain#getPrivateKey](https://developer.android.com/reference/kotlin/android/security/KeyChain.html#getPrivateKey(android.content.Context,%20kotlin.String))to receive the key. An example implementation of client certificates can be seen at [AOSP Browser](https://android.googlesource.com/platform/packages/apps/Browser/+/android-5.1.1_r1/src/com/android/browser/Tab.java) The default behavior is to cancel, returning no client certificate.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView that is initiating the callback |
| `request` | [ClientCertRequest](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest)!:An instance of a [ClientCertRequest](https://developer.android.com/reference/kotlin/android/webkit/ClientCertRequest) |

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
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView that is initiating the callback. |
| `request` | [WebResourceRequest](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest)!:The originating request. |
| `error` | [WebResourceError](https://developer.android.com/reference/kotlin/android/webkit/WebResourceError)!:Information about the error occurred. |

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

**Deprecated:** *Use [onReceivedError(WebView, WebResourceRequest, WebResourceError)](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onReceivedError(android.webkit.WebView,%20android.webkit.WebResourceRequest,%20android.webkit.WebResourceError))on [android.os.Build.VERSION_CODES#M](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int) and above.*

Report an error to the host application. These errors are unrecoverable (i.e. the main resource is unavailable). The`errorCode`parameter corresponds to one of the`ERROR_*`constants.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView that is initiating the callback. |
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The error code corresponding to an ERROR_\* value. |
| `description` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A String describing the error. |
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

Notifies the host application that the WebView received an HTTP authentication request. The host application can use the supplied [HttpAuthHandler](https://developer.android.com/reference/kotlin/android/webkit/HttpAuthHandler) to set the WebView's response to the request. The default behavior is to cancel the request.

**Note:**The supplied HttpAuthHandler must be used on the UI thread.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:the WebView that is initiating the callback |
| `handler` | [HttpAuthHandler](https://developer.android.com/reference/kotlin/android/webkit/HttpAuthHandler)!:the HttpAuthHandler used to set the WebView's response |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the host requiring authentication |
| `realm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the realm for which authentication is required |

**See Also**

- [android.webkit.WebView#getHttpAuthUsernamePassword](https://developer.android.com/reference/kotlin/android/webkit/WebView#getHttpAuthUsernamePassword(kotlin.String,%20kotlin.String)) 

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
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView that is initiating the callback. |
| `request` | [WebResourceRequest](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest)!:The originating request. |
| `errorResponse` | [WebResourceResponse](https://developer.android.com/reference/kotlin/android/webkit/WebResourceResponse)!:Information about the error occurred. |

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
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView requesting the login. |
| `realm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The account realm used to look up accounts. |
| `account` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:An optional account. If not`null`, the account should be checked against accounts on the device. If it is a valid account, it should be used to log in the user. |
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

Notifies the host application that an SSL error occurred while loading a resource. The host application must call either [SslErrorHandler.cancel()](https://developer.android.com/reference/kotlin/android/webkit/SslErrorHandler#cancel())or [SslErrorHandler.proceed()](https://developer.android.com/reference/kotlin/android/webkit/SslErrorHandler#proceed()).

**Warning:** Application overrides of this method can be used to display custom error pages or to silently log issues, but the host application should always call`SslErrorHandler#cancel()`and never proceed past errors.

**Note:** Do not prompt the user about SSL errors. Users are unlikely to be able to make an informed security decision, and`WebView`does not provide a UI for showing the details of the error in a meaningful way.

The decision to call`proceed()`or`cancel()`may be retained to facilitate responses to future SSL errors. The default behavior is to cancel the resource loading process.

This API is called only for recoverable SSL certificate errors. For non-recoverable errors (such as when the server fails the client), the`WebView`calls [onReceivedError(WebView,](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onReceivedError(android.webkit.WebView,%20android.webkit.WebResourceRequest,%20android.webkit.WebResourceError))with the [ERROR_FAILED_SSL_HANDSHAKE](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#ERROR_FAILED_SSL_HANDSHAKE:kotlin.Int) argument.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:`WebView`that initiated the callback. |
| `handler` | [SslErrorHandler](https://developer.android.com/reference/kotlin/android/webkit/SslErrorHandler)!: [SslErrorHandler](https://developer.android.com/reference/kotlin/android/webkit/SslErrorHandler) that handles the user's response. |
| `error` | [SslError](https://developer.android.com/reference/kotlin/android/net/http/SslError.html#)!:SSL error object. |

### onRenderProcessGone

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRenderProcessGone(
    view: WebView!, 
    detail: RenderProcessGoneDetail!
): Boolean
```

Notify host application that the given WebView's render process has exited. Multiple WebView instances may be associated with a single render process; onRenderProcessGone will be called for each WebView that was affected. The application's implementation of this callback should only attempt to clean up the specific WebView given as a parameter, and should not assume that other WebView instances are affected. The given WebView can't be used, and should be removed from the view hierarchy, all references to it should be cleaned up, e.g any references in the Activity or other classes saved using [android.view.View#findViewById](https://developer.android.com/reference/kotlin/android/view/View.html#findViewById(kotlin.Int))and similar calls, etc. To cause an render process crash for test purpose, the application can call`loadUrl("chrome://crash")`on the WebView. Note that multiple WebView instances may be affected if they share a render process, not just the specific WebView which loaded chrome://crash.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView which needs to be cleaned up. |
| `detail` | [RenderProcessGoneDetail](https://developer.android.com/reference/kotlin/android/webkit/RenderProcessGoneDetail)!:the reason why it exited. |

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

Notify the host application that a loading URL has been flagged by Safe Browsing. The application must invoke the callback to indicate the preferred response. The default behavior is to show an interstitial to the user, with the reporting checkbox visible. If the application needs to show its own custom interstitial UI, the callback can be invoked asynchronously with [SafeBrowsingResponse.backToSafety](https://developer.android.com/reference/kotlin/android/webkit/SafeBrowsingResponse#backToSafety(kotlin.Boolean))or [android.webkit.SafeBrowsingResponse#proceed](https://developer.android.com/reference/kotlin/android/webkit/SafeBrowsingResponse#proceed(kotlin.Boolean)), depending on user response.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView that hit the malicious resource. |
| `request` | [WebResourceRequest](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest)!:Object containing the details of the request. |
| `threatType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The reason the resource was caught by Safe Browsing, corresponding to a`SAFE_BROWSING_THREAT_*`value. Value is [android.webkit.WebViewClient#SAFE_BROWSING_THREAT_UNKNOWN](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#SAFE_BROWSING_THREAT_UNKNOWN:kotlin.Int), [android.webkit.WebViewClient#SAFE_BROWSING_THREAT_MALWARE](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#SAFE_BROWSING_THREAT_MALWARE:kotlin.Int), [android.webkit.WebViewClient#SAFE_BROWSING_THREAT_PHISHING](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#SAFE_BROWSING_THREAT_PHISHING:kotlin.Int), [android.webkit.WebViewClient#SAFE_BROWSING_THREAT_UNWANTED_SOFTWARE](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#SAFE_BROWSING_THREAT_UNWANTED_SOFTWARE:kotlin.Int), or [android.webkit.WebViewClient#SAFE_BROWSING_THREAT_BILLING](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#SAFE_BROWSING_THREAT_BILLING:kotlin.Int) |
| `callback` | [SafeBrowsingResponse](https://developer.android.com/reference/kotlin/android/webkit/SafeBrowsingResponse)!:Applications must invoke one of the callback methods. |

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
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView that is initiating the callback. |
| `oldScale` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The old scale factor |
| `newScale` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The new scale factor |

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
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView that is initiating the callback. |
| `cancelMsg` | [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)!:The message to send if the host wants to cancel |
| `continueMsg` | [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)!:The message to send if the host wants to continue |

### onUnhandledKeyEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onUnhandledKeyEvent(
    view: WebView!, 
    event: KeyEvent!
): Unit
```

Notify the host application that a key was not handled by the WebView. Except system keys, WebView always consumes the keys in the normal flow or if [shouldOverrideKeyEvent](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#shouldOverrideKeyEvent(android.webkit.WebView,%20android.view.KeyEvent))returns`true`. This is called asynchronously from where the key is dispatched. It gives the host application a chance to handle the unhandled key events.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView that is initiating the callback. |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!:The key event. |

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

**Note:** When Safe Browsing is enabled, these URLs still undergo Safe Browsing checks. If this is undesired, you can use [WebView.setSafeBrowsingWhitelist](https://developer.android.com/reference/kotlin/android/webkit/WebView#setSafeBrowsingWhitelist(kotlin.collections.MutableList,%20android.webkit.ValueCallback))to skip Safe Browsing checks for that host or dismiss the warning in [onSafeBrowsingHit](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onSafeBrowsingHit(android.webkit.WebView,%20android.webkit.WebResourceRequest,%20kotlin.Int,%20android.webkit.SafeBrowsingResponse))by calling [SafeBrowsingResponse.proceed](https://developer.android.com/reference/kotlin/android/webkit/SafeBrowsingResponse#proceed(kotlin.Boolean)).

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The [android.webkit.WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView) that is requesting the resource. |
| `request` | [WebResourceRequest](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest)!:Object containing the details of the request. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WebResourceResponse](https://developer.android.com/reference/kotlin/android/webkit/WebResourceResponse)? | A [android.webkit.WebResourceResponse](https://developer.android.com/reference/kotlin/android/webkit/WebResourceResponse) containing the response information or`null`if the WebView should load the resource itself. |

### shouldInterceptRequest

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shouldInterceptRequest(
    view: WebView!, 
    url: String!
): WebResourceResponse?
```

**Deprecated:** *Use [shouldInterceptRequest(WebView, WebResourceRequest)](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#shouldInterceptRequest(android.webkit.WebView,%20android.webkit.WebResourceRequest))on [android.os.Build.VERSION_CODES#M](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int) and above.*

Notify the host application of a resource request and allow the application to return the data. If the return value is`null`, the WebView will continue to load the resource as usual. Otherwise, the return response and data will be used.

This callback is invoked for a variety of URL schemes (e.g.,`http(s):`,`data:`,`file:`, etc.), not only those schemes which send requests over the network. This is not called for`javascript:`URLs,`blob:`URLs, or for assets accessed via`file:///android_asset/`or`file:///android_res/`URLs.

In the case of redirects, this is only called for the initial resource URL, not any subsequent redirect URLs.

**Note:**This method is called on a thread other than the UI thread so clients should exercise caution when accessing private data or the view system.

**Note:** When Safe Browsing is enabled, these URLs still undergo Safe Browsing checks. If this is undesired, you can use [WebView.setSafeBrowsingWhitelist](https://developer.android.com/reference/kotlin/android/webkit/WebView#setSafeBrowsingWhitelist(kotlin.collections.MutableList,%20android.webkit.ValueCallback))to skip Safe Browsing checks for that host or dismiss the warning in [onSafeBrowsingHit](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#onSafeBrowsingHit(android.webkit.WebView,%20android.webkit.WebResourceRequest,%20kotlin.Int,%20android.webkit.SafeBrowsingResponse))by calling [SafeBrowsingResponse.proceed](https://developer.android.com/reference/kotlin/android/webkit/SafeBrowsingResponse#proceed(kotlin.Boolean)).

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The [android.webkit.WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView) that is requesting the resource. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The raw url of the resource. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WebResourceResponse](https://developer.android.com/reference/kotlin/android/webkit/WebResourceResponse)? | A [android.webkit.WebResourceResponse](https://developer.android.com/reference/kotlin/android/webkit/WebResourceResponse) containing the response information or`null`if the WebView should load the resource itself. |

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
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView that is initiating the callback. |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!:The key event. |

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

**Note:** Do not call [WebView.loadUrl(String)](https://developer.android.com/reference/kotlin/android/webkit/WebView#loadUrl(kotlin.String))with the request's URL and then return`true`. This unnecessarily cancels the current load and starts a new load with the same URL. The correct way to continue loading a given URL is to simply return`false`, without calling [WebView.loadUrl(String)](https://developer.android.com/reference/kotlin/android/webkit/WebView#loadUrl(kotlin.String)).

**Note:**This method is not called for POST requests.

**Note:** This method may be called for subframes and with non-HTTP(S) schemes; calling [WebView.loadUrl(String)](https://developer.android.com/reference/kotlin/android/webkit/WebView#loadUrl(kotlin.String))with such a URL will fail.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView that is initiating the callback. |
| `request` | [WebResourceRequest](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest)!:Object containing the details of the request. |

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

**Deprecated:** *Use [shouldOverrideUrlLoading(WebView, WebResourceRequest)](https://developer.android.com/reference/kotlin/android/webkit/WebViewClient#shouldOverrideUrlLoading(android.webkit.WebView,%20android.webkit.WebResourceRequest))on [android.os.Build.VERSION_CODES#N](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int) and above.*

Give the host application a chance to take control when a URL is about to be loaded in the current WebView. If a WebViewClient is not provided, by default WebView will ask Activity Manager to choose the proper handler for the URL. If a WebViewClient is provided, returning`true`causes the current WebView to abort loading the URL, while returning`false`causes the WebView to continue loading the URL as usual.

**Note:** Do not call [WebView.loadUrl(String)](https://developer.android.com/reference/kotlin/android/webkit/WebView#loadUrl(kotlin.String))with the same URL and then return`true`. This unnecessarily cancels the current load and starts a new load with the same URL. The correct way to continue loading a given URL is to simply return`false`, without calling [WebView.loadUrl(String)](https://developer.android.com/reference/kotlin/android/webkit/WebView#loadUrl(kotlin.String)).

**Note:**This method is not called for POST requests.

**Note:** This method may be called for subframes and with non-HTTP(S) schemes; calling [WebView.loadUrl(String)](https://developer.android.com/reference/kotlin/android/webkit/WebView#loadUrl(kotlin.String))with such a URL will fail.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------|
| `view` | [WebView](https://developer.android.com/reference/kotlin/android/webkit/WebView)!:The WebView that is initiating the callback. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The URL to be loaded. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`to cancel the current load, otherwise return`false`. |
