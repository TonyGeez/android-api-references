# FillCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FillCallback

Kotlin| [Java](../android/service/autofill/FillCallback.md) 
| --- | --- |

```
class FillCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.FillCallback](../android/service/autofill/FillCallback.md) |

`FillCallback`handles autofill requests from the [AutofillService](../android/service/autofill/AutofillService.md) into the [Activity](../android/app/Activity.md) being autofilled.

To learn about using Autofill services in your app, read [Build autofill services](../guide/topics/text/autofill-services.md).

## Summary

| Public methods ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFailure](../android/service/autofill/FillCallback.md))`(`message:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Notifies the Android System that a fill request ([AutofillService.onFillRequest(FillRequest, android.os.CancellationSignal,](../android/service/autofill/AutofillService.md))) could not be fulfilled by the service (for example, because the user data was not available yet), so the request could be retried later. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSuccess](../android/service/autofill/FillCallback.md))`(`response:` ` [FillResponse](../android/service/autofill/FillResponse.md)?`)` Notifies the Android System that a fill request ([AutofillService.onFillRequest(FillRequest, android.os.CancellationSignal,](../android/service/autofill/AutofillService.md))) was successfully fulfilled by the service. |

## Public methods

### onFailure

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onFailure(message: CharSequence?): Unit
```

Notifies the Android System that a fill request ([AutofillService.onFillRequest(FillRequest, android.os.CancellationSignal,](../android/service/autofill/AutofillService.md))) could not be fulfilled by the service (for example, because the user data was not available yet), so the request could be retried later.

**Note:** this method should not be used when the service didn't have the heursitics to fulfill the request; in this case, the service should call [onSuccess(null)](../android/service/autofill/FillCallback.md))instead.

**Note:** prior to [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md), this method was not working as intended and the service should always call [onSuccess(null)](../android/service/autofill/FillCallback.md))instead.

**Note:** for apps targeting [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md) or higher, this method just logs the message on`logcat`; for apps targetting older SDKs, it also displays the message to user using a [android.widget.Toast](../android/widget/Toast.md). Generally speaking, you should not display an error to the user if the request failed, unless the request had the [FillRequest.FLAG_MANUAL_REQUEST](../android/service/autofill/FillRequest.md) flag.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:error message.**Note:** this message should**not** contain PII (Personally Identifiable Information, such as username or email address). This value may be`null`. |

| Exceptions ||
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this method or [onSuccess(android.service.autofill.FillResponse)](../android/service/autofill/FillCallback.md))was already called. |

### onSuccess

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun onSuccess(response: FillResponse?): Unit
```

Notifies the Android System that a fill request ([AutofillService.onFillRequest(FillRequest, android.os.CancellationSignal,](../android/service/autofill/AutofillService.md))) was successfully fulfilled by the service.

This method should always be called, even if the service doesn't have the heuristics to fulfill the request (in which case it should be called with`null`).

See the main [AutofillService](../android/service/autofill/AutofillService.md) documentation for more details and examples.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `response` | [FillResponse](../android/service/autofill/FillResponse.md)?:autofill information for that activity, or`null`when the service cannot autofill the activity. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this method or [onFailure(java.lang.CharSequence)](../android/service/autofill/FillCallback.md))was already called. |
