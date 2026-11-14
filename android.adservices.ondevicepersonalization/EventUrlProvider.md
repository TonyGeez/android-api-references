Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EventUrlProvider

```
open class EventUrlProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.EventUrlProvider](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventUrlProvider#) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The ODP APIs are deprecated and will not be supported in future Android releases. There is no direct replacement API available. Developers currently integrated with these APIs must cease further integration efforts. For comprehensive details regarding this deprecation and the future roadmap of Privacy Sandbox on Android, please consult the official Privacy Sandbox developer documentation and announcements: <https://privacysandbox.google.com>

Generates event tracking URLs for a request. The service can embed these URLs within the HTML output as needed. When the HTML is rendered within an ODP WebView, ODP will intercept requests to these URLs, call `IsolatedWorker#onEvent(EventInput, android.os.OutcomeReceiver)`, and log the returned output in the EVENTS table.

## Summary

| Public methods ||
|---|---|
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventUrlProvider#createEventTrackingUrlWithRedirect(android.os.PersistableBundle,%20android.net.Uri)(eventParams: https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#, destinationUrl: https://developer.android.com/reference/kotlin/android/net/Uri.html#?)` Creates an event tracking URL that redirects to the provided destination URL when it is clicked in an ODP webview. |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventUrlProvider#createEventTrackingUrlWithResponse(android.os.PersistableBundle,%20kotlin.ByteArray,%20kotlin.String)(eventParams: https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#, responseData: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?, mimeType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Creates an event tracking URL that returns the provided response. |

## Public methods

### createEventTrackingUrlWithRedirect

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createEventTrackingUrlWithRedirect(
    eventParams: PersistableBundle, 
    destinationUrl: Uri?
): Uri
```

**Deprecated:** *Deprecated in Java.*

Creates an event tracking URL that redirects to the provided destination URL when it is clicked in an ODP webview. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `eventParams` | [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#): The data to be passed to `IsolatedWorker#onEvent(EventInput, android.os.OutcomeReceiver)` when the event occurs. This value cannot be `null`. |
| `destinationUrl` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?: The URL to redirect to. This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#` | An ODP event URL that can be inserted into a WebView. This value cannot be `null`. |

### createEventTrackingUrlWithResponse

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createEventTrackingUrlWithResponse(
    eventParams: PersistableBundle, 
    responseData: ByteArray?, 
    mimeType: String?
): Uri
```

**Deprecated:** *Deprecated in Java.*

Creates an event tracking URL that returns the provided response. Returns HTTP Status 200 (OK) if the response data is not empty. Returns HTTP Status 204 (No Content) if the response data is empty. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---|---|
| `eventParams` | [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#): The data to be passed to `IsolatedWorker#onEvent(EventInput, android.os.OutcomeReceiver)` when the event occurs. This value cannot be `null`. |
| `responseData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: The content to be returned to the WebView when the URL is fetched. This value may be `null`. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The Mime Type of the URL response. This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#` | An ODP event URL that can be inserted into a WebView. This value cannot be `null`. |
