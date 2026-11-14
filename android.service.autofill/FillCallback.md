# FillCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FillCallback

Kotlin| [Java](https://developer.android.com/reference/android/service/autofill/FillCallback "View this page in Java") 

```
class FillCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.autofill.FillCallback](https://developer.android.com/reference/kotlin/android/service/autofill/FillCallback#) |

`FillCallback`handles autofill requests from the [AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService) into the [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) being autofilled.

To learn about using Autofill services in your app, read [Build autofill services](https://developer.android.com/reference/kotlin/guide/topics/text/autofill-services).

## Summary

| Public methods ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFailure](https://developer.android.com/reference/kotlin/android/service/autofill/FillCallback#onFailure(kotlin.CharSequence))`(`message:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Notifies the Android System that a fill request ([AutofillService.onFillRequest(FillRequest, android.os.CancellationSignal,](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onFillRequest(android.service.autofill.FillRequest,%20android.os.CancellationSignal,%20android.service.autofill.FillCallback))) could not be fulfilled by the service (for example, because the user data was not available yet), so the request could be retried later. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuccess](https://developer.android.com/reference/kotlin/android/service/autofill/FillCallback#onSuccess(android.service.autofill.FillResponse))`(`response:` ` [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse)?`)` Notifies the Android System that a fill request ([AutofillService.onFillRequest(FillRequest, android.os.CancellationSignal,](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onFillRequest(android.service.autofill.FillRequest,%20android.os.CancellationSignal,%20android.service.autofill.FillCallback))) was successfully fulfilled by the service. |

## Public methods

### onFailure

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onFailure(message: CharSequence?): Unit
```

Notifies the Android System that a fill request ([AutofillService.onFillRequest(FillRequest, android.os.CancellationSignal,](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onFillRequest(android.service.autofill.FillRequest,%20android.os.CancellationSignal,%20android.service.autofill.FillCallback))) could not be fulfilled by the service (for example, because the user data was not available yet), so the request could be retried later.

**Note:** this method should not be used when the service didn't have the heursitics to fulfill the request; in this case, the service should call [onSuccess(null)](https://developer.android.com/reference/kotlin/android/service/autofill/FillCallback#onSuccess(android.service.autofill.FillResponse))instead.

**Note:** prior to [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int), this method was not working as intended and the service should always call [onSuccess(null)](https://developer.android.com/reference/kotlin/android/service/autofill/FillCallback#onSuccess(android.service.autofill.FillResponse))instead.

**Note:** for apps targeting [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int) or higher, this method just logs the message on`logcat`; for apps targetting older SDKs, it also displays the message to user using a [android.widget.Toast](https://developer.android.com/reference/kotlin/android/widget/Toast.html#). Generally speaking, you should not display an error to the user if the request failed, unless the request had the [FillRequest.FLAG_MANUAL_REQUEST](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest#FLAG_MANUAL_REQUEST:kotlin.Int) flag.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:error message.**Note:** this message should**not** contain PII (Personally Identifiable Information, such as username or email address). This value may be`null`. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this method or [onSuccess(android.service.autofill.FillResponse)](https://developer.android.com/reference/kotlin/android/service/autofill/FillCallback#onSuccess(android.service.autofill.FillResponse))was already called. |

### onSuccess

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onSuccess(response: FillResponse?): Unit
```

Notifies the Android System that a fill request ([AutofillService.onFillRequest(FillRequest, android.os.CancellationSignal,](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onFillRequest(android.service.autofill.FillRequest,%20android.os.CancellationSignal,%20android.service.autofill.FillCallback))) was successfully fulfilled by the service.

This method should always be called, even if the service doesn't have the heuristics to fulfill the request (in which case it should be called with`null`).

See the main [AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService) documentation for more details and examples.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `response` | [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse)?:autofill information for that activity, or`null`when the service cannot autofill the activity. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this method or [onFailure(java.lang.CharSequence)](https://developer.android.com/reference/kotlin/android/service/autofill/FillCallback#onFailure(kotlin.CharSequence))was already called. |
