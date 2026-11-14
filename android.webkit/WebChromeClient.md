Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebChromeClient

Kotlin | [Java](WebChromeClient.md)
| --- | --- |

```
open class WebChromeClient
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.WebChromeClient](WebChromeClient.md) |

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/webkit/WebChromeClient.CustomViewCallback` A callback interface used by the host application to notify the current page that its custom view has been dismissed. |
| abstract | `https://developer.android.com/reference/kotlin/android/webkit/WebChromeClient.FileChooserParams` Parameters used in the onShowFileChooser method. |

| Public constructors ||
|---|---|
| WebChromeClient <br /> |

| Public methods ||
|---|---|
| open [Bitmap](../android.graphics/Bitmap.md)? | getDefaultVideoPoster When not playing, video elements are represented by a 'poster' image. |
| open [View](../android.view/View.md)? | getVideoLoadingProgressView Obtains a View to be displayed while buffering of full screen video is taking place. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | getVisitedHistory Obtains a list of all visited history items, used for link coloring |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onCloseWindow Notify the host application to close the given WebView and remove it from the view system if necessary. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onConsoleMessage Report a JavaScript console message to the host application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onConsoleMessage Report a JavaScript error message to the host application. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onCreateWindow Request the host application to create a new window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onExceededDatabaseQuota Tell the client that the quota has been exceeded for the Web SQL Database API for a particular origin and request a new quota. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onGeolocationPermissionsHidePrompt Notify the host application that a request for Geolocation permissions, made with a previous call to onGeolocationPermissionsShowPrompt has been canceled. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onGeolocationPermissionsShowPrompt Notify the host application that web content from the specified origin is attempting to use the Geolocation API, but no permission state is currently set for that origin. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onHideCustomView Notify the host application that the current page has exited full screen mode. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onJsAlert Notify the host application that the web page wants to display a JavaScript `alert()` dialog. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onJsBeforeUnload Notify the host application that the web page wants to confirm navigation from JavaScript `onbeforeunload`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onJsConfirm Notify the host application that the web page wants to display a JavaScript `confirm()` dialog. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onJsPrompt Notify the host application that the web page wants to display a JavaScript `prompt()` dialog. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onJsTimeout Tell the client that a JavaScript execution timeout has occured. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onPermissionRequest Notify the host application that web content is requesting permission to access the specified resources and the permission currently isn't granted or denied. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onPermissionRequestCanceled Notify the host application that the given permission request has been canceled. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onProgressChanged Tell the host application the current progress of loading a page. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onReceivedIcon Notify the host application of a new favicon for the current page. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onReceivedTitle Notify the host application of a change in the document title. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onReceivedTouchIconUrl Notify the host application of the url for an apple-touch-icon. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onRequestFocus Request display and focus for this WebView. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onShowCustomView Notify the host application that the current page has entered full screen mode. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onShowCustomView Notify the host application that the current page would like to show a custom View in a particular orientation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onShowFileChooser Asks the client app to show a file chooser. |

## Public constructors

### WebChromeClient

```
WebChromeClient()
```

## Public methods

### getDefaultVideoPoster

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDefaultVideoPoster(): Bitmap?
```

When not playing, video elements are represented by a 'poster' image. The image to use can be specified by the poster attribute of the video tag in HTML. If the attribute is absent, then a default poster will be used. This method allows the ChromeClient to provide that default image.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#?` | Bitmap The image to use as a default poster, or `null` if no such image is available. |

### getVideoLoadingProgressView

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVideoLoadingProgressView(): View?
```

Obtains a View to be displayed while buffering of full screen video is taking place. The host application can override this method to provide a View containing a spinner or similar.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View.html#?` | View The View to be displayed whilst the video is loading. This value may be `null`. |

### getVisitedHistory

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVisitedHistory(callback: ValueCallback<Array<String!>!>!): Unit
```

Obtains a list of all visited history items, used for link coloring

### onCloseWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCloseWindow(window: WebView!): Unit
```

Notify the host application to close the given WebView and remove it from the view system if necessary. At this point, WebCore has stopped any loading in this window and has removed any cross-scripting ability in javascript.

As with onCreateWindow, the application should ensure that any URL or security indicator displayed is updated so that the user can tell that the page they were interacting with has been closed.

| Parameters ||
|---|---|
| `window` | [WebView](WebView.md)!: The WebView that needs to be closed. |

### onConsoleMessage

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onConsoleMessage(consoleMessage: ConsoleMessage!): Boolean
```

Report a JavaScript console message to the host application. The ChromeClient should override this to process the log message as they see fit.

| Parameters ||
|---|---|
| `consoleMessage` | [ConsoleMessage](ConsoleMessage.md)!: Object containing details of the console message. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the message is handled by the client. |

### onConsoleMessage

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onConsoleMessage(
    message: String!, 
    lineNumber: Int, 
    sourceID: String!
): Unit
```

**Deprecated:** *Use onConsoleMessage instead.*

Report a JavaScript error message to the host application. The ChromeClient should override this to process the log message as they see fit.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The error message to report. |
| `lineNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The line number of the error. |
| `sourceID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the source file that caused the error. |
| --- | --- |

### onCreateWindow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateWindow(
    view: WebView!, 
    isDialog: Boolean, 
    isUserGesture: Boolean, 
    resultMsg: Message!
): Boolean
```

Request the host application to create a new window. If the host application chooses to honor this request, it should return `true` from this method, create a new WebView to host the window, insert it into the View system and send the supplied resultMsg message to its target with the new WebView as an argument. If the host application chooses not to honor the request, it should return `false` from this method. The default implementation of this method does nothing and hence returns `false`.

Applications should typically not allow windows to be created when the `isUserGesture` flag is false, as this may be an unwanted popup.

Applications should be careful how they display the new window: don't simply overlay it over the existing WebView as this may mislead the user about which site they are viewing. If your application displays the URL of the main page, make sure to also display the URL of the new window in a similar fashion. If your application does not display URLs, consider disallowing the creation of new windows entirely.

**Note:** There is no trustworthy way to tell which page requested the new window: the request might originate from a third-party iframe inside the WebView.

| Parameters ||
|---|---|
| `view` | [WebView](WebView.md)!: The WebView from which the request for a new window originated. |
| `isDialog` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the new window should be a dialog, rather than a full-size window. |
| `isUserGesture` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the request was initiated by a user gesture, such as the user clicking a link. |
| --- | --- |
| `resultMsg` | [Message](../android.os/Message.md)!: The message to send when once a new WebView has been created. resultMsg.obj is a `https://developer.android.com/reference/kotlin/android/webkit/WebView.WebViewTransport` object. This should be used to transport the new WebView, by calling setWebView. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | This method should return `true` if the host application will create a new window, in which case resultMsg should be sent to its target. Otherwise, this method should return `false`. Returning `false` from this method but also sending resultMsg will result in undefined behavior. |

### onExceededDatabaseQuota

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onExceededDatabaseQuota(
    url: String!, 
    databaseIdentifier: String!, 
    quota: Long, 
    estimatedDatabaseSize: Long, 
    totalQuota: Long, 
    quotaUpdater: WebStorage.QuotaUpdater!
): Unit
```

**Deprecated:** *This method is no longer called; WebView now uses the HTML5 / JavaScript Quota Management API.*

Tell the client that the quota has been exceeded for the Web SQL Database API for a particular origin and request a new quota. The client must respond by invoking the updateQuota method of the supplied `https://developer.android.com/reference/kotlin/android/webkit/WebStorage.QuotaUpdater` instance. The minimum value that can be set for the new quota is the current quota. The default implementation responds with the current quota, so the quota will not be increased.

| Parameters ||
|---|---|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The URL of the page that triggered the notification |
| `databaseIdentifier` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The identifier of the database where the quota was exceeded. |
| `quota` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The quota for the origin, in bytes |
| --- | --- |
| `estimatedDatabaseSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The estimated size of the offending database, in bytes |
| `totalQuota` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The total quota for all origins, in bytes |
| `quotaUpdater` | [WebStorage.QuotaUpdater](../android/webkit/WebStorage.QuotaUpdater.md)!: An instance of `https://developer.android.com/reference/kotlin/android/webkit/WebStorage.QuotaUpdater` which must be used to inform the WebView of the new quota. |
| --- | --- |

### onGeolocationPermissionsHidePrompt

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onGeolocationPermissionsHidePrompt(): Unit
```

Notify the host application that a request for Geolocation permissions, made with a previous call to onGeolocationPermissionsShowPrompt has been canceled. Any related UI should therefore be hidden.

### onGeolocationPermissionsShowPrompt

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onGeolocationPermissionsShowPrompt(
    origin: String!, 
    callback: GeolocationPermissions.Callback!
): Unit
```

Notify the host application that web content from the specified origin is attempting to use the Geolocation API, but no permission state is currently set for that origin. The host application should invoke the specified callback with the desired permission state. See GeolocationPermissions for details.

Note that for applications targeting Android N and later SDKs (API level \> `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`) this method is only called for requests originating from secure origins such as https. On non-secure origins geolocation requests are automatically denied.

| Parameters ||
|---|---|
| `origin` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The origin of the web content attempting to use the Geolocation API. |
| `callback` | [GeolocationPermissions.Callback](../android/webkit/GeolocationPermissions.Callback.md)!: The callback to use to set the permission state for the origin. |

### onHideCustomView

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onHideCustomView(): Unit
```

Notify the host application that the current page has exited full screen mode. The host application must hide the custom View (the View which was previously passed to onShowCustomView). After this call, web content will render in the original WebView again.

**Note:** if overriding this method, the application must also override onShowCustomView.

### onJsAlert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onJsAlert(
    view: WebView!, 
    url: String!, 
    message: String!, 
    result: JsResult!
): Boolean
```

Notify the host application that the web page wants to display a JavaScript `alert()` dialog.

The default behavior if this method returns `false` or is not overridden is to show a dialog containing the alert message and suspend JavaScript execution until the dialog is dismissed.

To show a custom dialog, the app should return `true` from this method, in which case the default dialog will not be shown and JavaScript execution will be suspended. The app should call `JsResult.confirm()` when the custom dialog is dismissed such that JavaScript execution can be resumed.

To suppress the dialog and allow JavaScript execution to continue, call `JsResult.confirm()` immediately and then return `true`.

Note that if the WebChromeClient is set to be `null`, or if WebChromeClient is not set at all, the default dialog will be suppressed and Javascript execution will continue immediately.

Note that the default dialog does not inherit the `https://developer.android.com/reference/kotlin/android/view/Display.html#FLAG_SECURE:kotlin.Int` flag from the parent window.

| Parameters ||
|---|---|
| `view` | [WebView](WebView.md)!: The WebView that initiated the callback. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The url of the page requesting the dialog. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Message to be displayed in the window. |
| --- | --- |
| `result` | [JsResult](JsResult.md)!: A JsResult to confirm that the user closed the window. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | boolean `true` if the request is handled or ignored. `false` if WebView needs to show the default dialog. |

### onJsBeforeUnload

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onJsBeforeUnload(
    view: WebView!, 
    url: String!, 
    message: String!, 
    result: JsResult!
): Boolean
```

Notify the host application that the web page wants to confirm navigation from JavaScript `onbeforeunload`.

The default behavior if this method returns `false` or is not overridden is to show a dialog containing the message and suspend JavaScript execution until the dialog is dismissed. The default dialog will continue the navigation if the user confirms the navigation, and will stop the navigation if the user wants to stay on the current page.

To show a custom dialog, the app should return `true` from this method, in which case the default dialog will not be shown and JavaScript execution will be suspended. When the custom dialog is dismissed, the app should call `JsResult.confirm()` to continue the navigation or, `JsResult.cancel()` to stay on the current page.

To suppress the dialog and allow JavaScript execution to continue, call `JsResult.confirm()` or `JsResult.cancel()` immediately and then return `true`.

Note that if the WebChromeClient is set to be `null`, or if WebChromeClient is not set at all, the default dialog will be suppressed and the navigation will be resumed immediately.

Note that the default dialog does not inherit the `https://developer.android.com/reference/kotlin/android/view/Display.html#FLAG_SECURE:kotlin.Int` flag from the parent window.

| Parameters ||
|---|---|
| `view` | [WebView](WebView.md)!: The WebView that initiated the callback. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The url of the page requesting the dialog. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Message to be displayed in the window. |
| --- | --- |
| `result` | [JsResult](JsResult.md)!: A JsResult used to send the user's response to javascript. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | boolean `true` if the request is handled or ignored. `false` if WebView needs to show the default dialog. |

### onJsConfirm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onJsConfirm(
    view: WebView!, 
    url: String!, 
    message: String!, 
    result: JsResult!
): Boolean
```

Notify the host application that the web page wants to display a JavaScript `confirm()` dialog.

The default behavior if this method returns `false` or is not overridden is to show a dialog containing the message and suspend JavaScript execution until the dialog is dismissed. The default dialog will return `true` to the JavaScript `confirm()` code when the user presses the 'confirm' button, and will return `false` to the JavaScript code when the user presses the 'cancel' button or dismisses the dialog.

To show a custom dialog, the app should return `true` from this method, in which case the default dialog will not be shown and JavaScript execution will be suspended. The app should call `JsResult.confirm()` or `JsResult.cancel()` when the custom dialog is dismissed.

To suppress the dialog and allow JavaScript execution to continue, call `JsResult.confirm()` or `JsResult.cancel()` immediately and then return `true`.

Note that if the WebChromeClient is set to be `null`, or if WebChromeClient is not set at all, the default dialog will be suppressed and the default value of `false` will be returned to the JavaScript code immediately.

Note that the default dialog does not inherit the `https://developer.android.com/reference/kotlin/android/view/Display.html#FLAG_SECURE:kotlin.Int` flag from the parent window.

| Parameters ||
|---|---|
| `view` | [WebView](WebView.md)!: The WebView that initiated the callback. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The url of the page requesting the dialog. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Message to be displayed in the window. |
| --- | --- |
| `result` | [JsResult](JsResult.md)!: A JsResult used to send the user's response to javascript. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | boolean `true` if the request is handled or ignored. `false` if WebView needs to show the default dialog. |

### onJsPrompt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onJsPrompt(
    view: WebView!, 
    url: String!, 
    message: String!, 
    defaultValue: String!, 
    result: JsPromptResult!
): Boolean
```

Notify the host application that the web page wants to display a JavaScript `prompt()` dialog.

The default behavior if this method returns `false` or is not overridden is to show a dialog containing the message and suspend JavaScript execution until the dialog is dismissed. Once the dialog is dismissed, JavaScript `prompt()` will return the string that the user typed in, or null if the user presses the 'cancel' button.

To show a custom dialog, the app should return `true` from this method, in which case the default dialog will not be shown and JavaScript execution will be suspended. The app should call `JsPromptResult.confirm(result)` when the custom dialog is dismissed.

To suppress the dialog and allow JavaScript execution to continue, call `JsPromptResult.confirm(result)` immediately and then return `true`.

Note that if the WebChromeClient is set to be `null`, or if WebChromeClient is not set at all, the default dialog will be suppressed and `null` will be returned to the JavaScript code immediately.

Note that the default dialog does not inherit the `https://developer.android.com/reference/kotlin/android/view/Display.html#FLAG_SECURE:kotlin.Int` flag from the parent window.

| Parameters ||
|---|---|
| `view` | [WebView](WebView.md)!: The WebView that initiated the callback. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The url of the page requesting the dialog. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Message to be displayed in the window. |
| --- | --- |
| `defaultValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The default value displayed in the prompt dialog. |
| `result` | [JsPromptResult](JsPromptResult.md)!: A JsPromptResult used to send the user's reponse to javascript. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | boolean `true` if the request is handled or ignored. `false` if WebView needs to show the default dialog. |

### onJsTimeout

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onJsTimeout(): Boolean
```

**Deprecated:** *This method is no longer supported and will not be invoked.*

Tell the client that a JavaScript execution timeout has occured. And the client may decide whether or not to interrupt the execution. If the client returns `true`, the JavaScript will be interrupted. If the client returns `false`, the execution will continue. Note that in the case of continuing execution, the timeout counter will be reset, and the callback will continue to occur if the script does not finish at the next check point.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | boolean Whether the JavaScript execution should be interrupted. |

### onPermissionRequest

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPermissionRequest(request: PermissionRequest!): Unit
```

Notify the host application that web content is requesting permission to access the specified resources and the permission currently isn't granted or denied. The host application must invoke grant or deny. If this method isn't overridden, the permission is denied.

| Parameters ||
|---|---|
| `request` | [PermissionRequest](PermissionRequest.md)!: the PermissionRequest from current web content. |

### onPermissionRequestCanceled

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPermissionRequestCanceled(request: PermissionRequest!): Unit
```

Notify the host application that the given permission request has been canceled. Any related UI should therefore be hidden.

| Parameters ||
|---|---|
| `request` | [PermissionRequest](PermissionRequest.md)!: the PermissionRequest that needs be canceled. |

### onProgressChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onProgressChanged(
    view: WebView!, 
    newProgress: Int
): Unit
```

Tell the host application the current progress of loading a page.

| Parameters ||
|---|---|
| `view` | [WebView](WebView.md)!: The WebView that initiated the callback. |
| `newProgress` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Current page loading progress, represented by an integer between 0 and 100. |

### onReceivedIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onReceivedIcon(
    view: WebView!, 
    icon: Bitmap!
): Unit
```

Notify the host application of a new favicon for the current page.

| Parameters ||
|---|---|
| `view` | [WebView](WebView.md)!: The WebView that initiated the callback. |
| `icon` | [Bitmap](../android.graphics/Bitmap.md)!: A Bitmap containing the favicon for the current page. |

### onReceivedTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onReceivedTitle(
    view: WebView!, 
    title: String!
): Unit
```

Notify the host application of a change in the document title.

| Parameters ||
|---|---|
| `view` | [WebView](WebView.md)!: The WebView that initiated the callback. |
| `title` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A String containing the new title of the document. |

### onReceivedTouchIconUrl

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onReceivedTouchIconUrl(
    view: WebView!, 
    url: String!, 
    precomposed: Boolean
): Unit
```

Notify the host application of the url for an apple-touch-icon.

| Parameters ||
|---|---|
| `view` | [WebView](WebView.md)!: The WebView that initiated the callback. |
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The icon url. |
| `precomposed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the url is for a precomposed touch icon. |
| --- | --- |

### onRequestFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onRequestFocus(view: WebView!): Unit
```

Request display and focus for this WebView. This may happen due to another WebView opening a link in this WebView and requesting that this WebView be displayed.

| Parameters ||
|---|---|
| `view` | [WebView](WebView.md)!: The WebView that needs to be focused. |

### onShowCustomView

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onShowCustomView(
    view: View!, 
    callback: WebChromeClient.CustomViewCallback!
): Unit
```

Notify the host application that the current page has entered full screen mode. After this call, web content will no longer be rendered in the WebView, but will instead be rendered in `view`. The host application should add this View to a Window which is configured with `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_FULLSCREEN:kotlin.Int` flag in order to actually display this web content full screen.

The application may explicitly exit fullscreen mode by invoking `callback` (ex. when the user presses the back button). However, this is generally not necessary as the web page will often show its own UI to close out of fullscreen. Regardless of how the WebView exits fullscreen mode, WebView will invoke onHideCustomView, signaling for the application to remove the custom View.

If this method is not overridden, WebView will report to the web page it does not support fullscreen mode and will not honor the web page's request to run in fullscreen mode.

**Note:** if overriding this method, the application must also override onHideCustomView.

| Parameters ||
|---|---|
| `view` | [View](../android.view/View.md)!: is the View object to be shown. |
| `callback` | [WebChromeClient.CustomViewCallback](../android/webkit/WebChromeClient.CustomViewCallback.md)!: invoke this callback to request the page to exit full screen mode. |

### onShowCustomView

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onShowCustomView(
    view: View!, 
    requestedOrientation: Int, 
    callback: WebChromeClient.CustomViewCallback!
): Unit
```

**Deprecated:** *This method supports the obsolete plugin mechanism, and will not be invoked in future*

Notify the host application that the current page would like to show a custom View in a particular orientation.

| Parameters ||
|---|---|
| `view` | [View](../android.view/View.md)!: is the View object to be shown. |
| `requestedOrientation` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An orientation constant as used in `https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#screenOrientation:kotlin.Int`. |
| `callback` | [WebChromeClient.CustomViewCallback](../android/webkit/WebChromeClient.CustomViewCallback.md)!: is the callback to be invoked if and when the view is dismissed. |
| --- | --- |

### onShowFileChooser

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onShowFileChooser(
    webView: WebView!, 
    filePathCallback: ValueCallback<Array<Uri!>!>!, 
    fileChooserParams: WebChromeClient.FileChooserParams!
): Boolean
```

Asks the client app to show a file chooser. The web page has requested to either upload or save a file, such as from a 'file' input in an HTML form or due to a JavaScript API call. The client app can decide whether to show the user a file chooser dialog or to programmatically handle the request. This can be invoked both for uploads and downloads, and it can also be invoked for single files, multiple files, or entire folders. Client apps should check `fileChooserParams` for details about what type of file is being requested.

To show the user a file chooser dialog, override this callback to return `true` and store the `filePathCallback` in a variable. Present the dialog to the user and when they reply, invoke the callback with a URI which points to the file. Make sure to check the `fileChooserParams` in order to show appropriate options in the file chooser dialog, such as automatically filtering by relevant file type (see getAcceptTypes).

To handle each request programmatically, respond to this callback with `true`. You can invoke `filePathCallback` with `null` in order to cancel the request or you can invoke the callback with a URI to actual file or folder.

The default behavior is that WebView will cancel all file requests.

**Note:** WebView does not enforce any restrictions on the chosen file(s). WebView can access all files that your app can access. In case the file(s) are chosen through an untrusted source such as a third-party app, it is your own app's responsibility to check what the returned Uris refer to before calling the `filePathCallback`. See createIntent and parseResult for more details.

| Parameters ||
|---|---|
| `webView` | [WebView](WebView.md)!: The WebView instance that is initiating the request. |
| `filePathCallback` | [ValueCallback](ValueCallback.md)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Uri](../android.net/Uri.md)!\>!\>!: Invoke this callback to supply the list of paths to files to upload, or `null` to cancel. Must only be called if the onShowFileChooser implementation returns `true`. |
| `fileChooserParams` | [WebChromeClient.FileChooserParams](../android/webkit/WebChromeClient.FileChooserParams.md)!: Describes the mode of file chooser to be opened, and options to be used with it. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if filePathCallback will be invoked, `false` to use default handling. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/webkit/WebChromeClient.FileChooserParams`
